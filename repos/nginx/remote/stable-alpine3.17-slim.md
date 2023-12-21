## `nginx:stable-alpine3.17-slim`

```console
$ docker pull nginx@sha256:14d581cfe9d840cfb28ac57e27f707cce3c95f7bfc1695b93c89a68b63a0b952
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

### `nginx:stable-alpine3.17-slim` - linux; amd64

```console
$ docker pull nginx@sha256:cfe1b60f0b014ed3e5d12896065559a9de4beea8ff7a14a73ce682a8b8050dc6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5182259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9d585bd0f8042ee9a01849de0db4d8fc613d84487eea795f4b2141848c481e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:80331a5d882ac8a70763f4b19e06f2e04ea3dca34ae6d92810815b170b3c806c in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"dc47dbaeb1c0874b264d34ddfec40e7d2b814e7db48d144e12d5991c743ef5fcf780ecbab72324e562dd84bb9c0e4dd71d14850b20ceaf470c46f8fe7510275b *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1207c741d8c9b028d98c4006013f9de959da3c55f85b91ed5e4583438a0112ca`  
		Last Modified: Thu, 30 Nov 2023 23:23:40 GMT  
		Size: 3.4 MB (3379323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd2102c9ad2d916fe72366eec215d071ef495d56fbf734ddf72a2cb6ed417a09`  
		Last Modified: Wed, 20 Dec 2023 20:14:12 GMT  
		Size: 1.8 MB (1799186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da95676acad4140839e6da3d2e65e3b8d889e1fb9062d17f7a994ce5e0ef3c1d`  
		Last Modified: Wed, 20 Dec 2023 20:14:11 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1b99f2ae09fdbea9279c95a5ccc88f38de9502e5fcf0c64b4ae8622b87f4710`  
		Last Modified: Wed, 20 Dec 2023 20:14:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d06f16a4976a005656585d1ede62a7006637816c80cbed5ea7f0a5b698d5074c`  
		Last Modified: Wed, 20 Dec 2023 20:14:12 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16dc7a3c36676a8f8f9c3a99153efeae1ab0781a89340411d732199a4de70017`  
		Last Modified: Wed, 20 Dec 2023 20:14:12 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.17-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:0a9bf385d51bd43dd36dfb2165a2abaa65da956d77ede1f2309ba1824bf18e3c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.4 KB (727377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ffab98b112933469c579f066aab9d4806c300d118ee2ad69288c1b4da912800`

```dockerfile
```

-	Layers:
	-	`sha256:779a34ff010435618d81bb75b461de4ed64f8f67069c2905a5af0167c647995f`  
		Last Modified: Wed, 20 Dec 2023 20:14:11 GMT  
		Size: 699.7 KB (699680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f32d0fac265af3dd42cd690ba837054485c41f28a856c6da88e534cd73231374`  
		Last Modified: Wed, 20 Dec 2023 20:14:11 GMT  
		Size: 27.7 KB (27697 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.17-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:bc776b3297bc66f8866c3e6a12da779d0caa7b10bef7c5213e1c059418a71200
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5010631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93de4398bea2d4490f7da0cf9ab77f8b8219d705792ded396062ca21a286bede`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:90d3bdc6a557ead63796de0110e2fda87e65aa091070cbae612dfb2126568253 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"dc47dbaeb1c0874b264d34ddfec40e7d2b814e7db48d144e12d5991c743ef5fcf780ecbab72324e562dd84bb9c0e4dd71d14850b20ceaf470c46f8fe7510275b *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f0440ff44d712e5fc701b84856116589b428157893ac461b633b1ab30b627eed`  
		Last Modified: Thu, 30 Nov 2023 22:49:52 GMT  
		Size: 3.1 MB (3113003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fd0f74d4b9cc96fa7587ffe6b6542849e5be84214fa83963a5f1664a5557eb`  
		Last Modified: Wed, 20 Dec 2023 22:00:31 GMT  
		Size: 1.9 MB (1893878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f415e03abb6e2495a8e3ebbfd31beb44102d34d9191c97c831335cd5ddf8e9ba`  
		Last Modified: Wed, 20 Dec 2023 22:00:31 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b7ac3a8e35946f4a6043081d08b86ee7b4c63a895903d428f63fa5f05e54c31`  
		Last Modified: Wed, 20 Dec 2023 22:00:31 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9ee0ead38a2db325f12e8fbf7c6e8a1f90417f0cab6e4c342f43b67668285ae`  
		Last Modified: Wed, 20 Dec 2023 22:00:31 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28bcbe69ae50c1d208b33b63d97fb05630c1f1aab654339f5946df633b60bf37`  
		Last Modified: Wed, 20 Dec 2023 22:00:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.17-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:65d3516af39a86e14fc9f51089254784210ea04f7cef7b51af5fcba2229f558c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 KB (27568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7094fe3fdabe7956b372621274fdea71726ebb5467b956392ff74ba52a6e8d71`

```dockerfile
```

-	Layers:
	-	`sha256:70e697bddeb1fec4eeb932a57f2714ae5407c5f61553599351a296ae330e08ef`  
		Last Modified: Wed, 20 Dec 2023 22:00:31 GMT  
		Size: 27.6 KB (27568 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.17-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:7d8034c604b6a3aef17cc51915b6d1c5fce69edb07d16ac87fa8ff733a46af64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.6 MB (4621867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aad1ebd5d03d815bd9dd0608123c9ede0ee70be00da728810a11b1d731eae47`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:02a6ccbee2a71a547141a8480f3a3912c7bb0934df31124f4a4720204d326698 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"dc47dbaeb1c0874b264d34ddfec40e7d2b814e7db48d144e12d5991c743ef5fcf780ecbab72324e562dd84bb9c0e4dd71d14850b20ceaf470c46f8fe7510275b *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d4ee79c42f17f258e1c67dc32e0776c934799d208cd0a9b6264f65d60f1a26fc`  
		Last Modified: Thu, 30 Nov 2023 22:50:08 GMT  
		Size: 2.9 MB (2869713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f2b0c7b922e8fcefc8cbe3c86fd472d292707210669ab4dd6e07f761fc3f0d4`  
		Last Modified: Wed, 20 Dec 2023 23:24:49 GMT  
		Size: 1.7 MB (1748403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f07516a8810e69c55c70fe5a7db85c36c2ea25319214637e2d7653ce341a745`  
		Last Modified: Wed, 20 Dec 2023 23:24:48 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7173d4d63ffa44a3013f7762d29674ed635ef9e05fa00c9e4329e3f555e1a7b`  
		Last Modified: Wed, 20 Dec 2023 23:24:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abde82b9e4380ae12868a56305549a11dfd875f9af3dfb51a76c2ed0b4244444`  
		Last Modified: Wed, 20 Dec 2023 23:24:48 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200a77b2c8e142c5fbd5e1fc50ce11fb801deda802ddde1fd546557c86001e7b`  
		Last Modified: Wed, 20 Dec 2023 23:24:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.17-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:5059920f84a3e65809040a76229885087c6e6946cfc74ec9d045119c79283bf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.3 KB (727349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f6563b235a9c1cde76392da23c25bad8b48d5952605cc38fdffa7afe96ea22`

```dockerfile
```

-	Layers:
	-	`sha256:a5267323823cc2b238592fd27bf5ca293949fb747f1e3fb768315e6d94874cd4`  
		Last Modified: Wed, 20 Dec 2023 23:24:49 GMT  
		Size: 699.7 KB (699732 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:701dd681435715dac302428e1c151517b19b75d3ab7f83ccab050a45f727dc70`  
		Last Modified: Wed, 20 Dec 2023 23:24:48 GMT  
		Size: 27.6 KB (27617 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.17-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:d46de553b9f592f29d0c80bea32f876fc20bb2e6cfff66a4e50659575581bf1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.1 MB (5050679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:459dc45ac269a784f83b6b2783f83aa6157589631195de018ee35dbce8a40bc8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:e5c66967d6570e36da50c9d42dd8f8f55e6c6a65b92c79601ea9e750c076fa2a in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"dc47dbaeb1c0874b264d34ddfec40e7d2b814e7db48d144e12d5991c743ef5fcf780ecbab72324e562dd84bb9c0e4dd71d14850b20ceaf470c46f8fe7510275b *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b8180c93b172865af87a7c0e7e3c8bcb139e0d0c92e19c96467ff2cd4c8919ad`  
		Last Modified: Thu, 30 Nov 2023 23:11:45 GMT  
		Size: 3.3 MB (3258348 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81c7735b56752911732abd78dec0e785932e152c1197a2494f3bedf55e21c745`  
		Last Modified: Wed, 20 Dec 2023 22:36:45 GMT  
		Size: 1.8 MB (1788584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8154ad53e97667b75978238f58fa65c2fd010d7dfc3436bfb5ef0ac1cc2d7ea`  
		Last Modified: Wed, 20 Dec 2023 22:36:45 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4f71b90d2764f5dfd30dbe72bede9e213d4791630b06c41f395444a8f00c1b`  
		Last Modified: Wed, 20 Dec 2023 22:36:45 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152e7550475912d5fe7bf49f919f2e8d441cf7013ce5fbfe5f6f989e4e835e9e`  
		Last Modified: Wed, 20 Dec 2023 22:36:45 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fce7eee88839b7de8f535d0d32a59e04491368fcdfcf268b0e5b40f6291f9b5c`  
		Last Modified: Wed, 20 Dec 2023 22:36:46 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.17-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:717dc7cd2f3e654fa00b5a73ec19933fdea70740860b2f6f609ed9c6eea6f9e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **727.4 KB (727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:888899c047a23766a2501ed39d28452b5497f5a08baca62302c6d7312da68ffd`

```dockerfile
```

-	Layers:
	-	`sha256:3f100099aa7509ab126329ad1582a62498b065418216baca86f7dadc1dd8fa9d`  
		Last Modified: Wed, 20 Dec 2023 22:36:45 GMT  
		Size: 699.7 KB (699695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:81223821812016b8396fdeb56a271e32dfe82a7b8d3b1188bd2faff1ef93d3ab`  
		Last Modified: Wed, 20 Dec 2023 22:36:45 GMT  
		Size: 27.7 KB (27711 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.17-slim` - linux; 386

```console
$ docker pull nginx@sha256:0fd0f5d215ce20af00a18d0a50043be47bb11bf14964eec5db2149a49ec7545b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5465184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:035736db038cf35815f4764e6111baea7cc68875e72c795b3b3045e4a6a6ce61`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:4ad1e09b0030ebbf09adcc7c616502a079dc61aff7c6edce2f2ea248cd85b2df in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"dc47dbaeb1c0874b264d34ddfec40e7d2b814e7db48d144e12d5991c743ef5fcf780ecbab72324e562dd84bb9c0e4dd71d14850b20ceaf470c46f8fe7510275b *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7583c43471b6e056e4cc98119de7f0921ba6ad8cd2645554165c3d9869b344dc`  
		Last Modified: Fri, 01 Dec 2023 02:04:31 GMT  
		Size: 3.4 MB (3414867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf2c95a244ab38ffe663a73e0fb55e6eec46909ef083e4a7d5bdd0392466d3b`  
		Last Modified: Wed, 20 Dec 2023 20:15:46 GMT  
		Size: 2.0 MB (2046563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f5a27f84b246e45f090a4dd92c5a8c635db1b2c7205d83e226c71eada8ac7b`  
		Last Modified: Wed, 20 Dec 2023 20:15:46 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f92919cac4cec12c29c6a0a778b4117e556212448da8d53ea59f8fc3f6597dd`  
		Last Modified: Wed, 20 Dec 2023 20:15:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ca79410bda2476edee6f0db68b7dd01e61d2a08613528e7ffc775a60f93f1b`  
		Last Modified: Wed, 20 Dec 2023 20:15:46 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a15382fbf5cb28956c96eb0c9d9305195161ea65fa3c08f0829d093332e4db0`  
		Last Modified: Wed, 20 Dec 2023 20:15:47 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.17-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:1e1b595bf1f0f39bc803d511923d208182f8d2a865ff83f4d56430417f3d4a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.4 KB (27443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6600a66d943660d31945fb8ae59798439287966ebec63045ba9509f7c02724a6`

```dockerfile
```

-	Layers:
	-	`sha256:0b3d45593e21c606099812498b90c97dd901f93ba7c69b81bafe169e02d553b7`  
		Last Modified: Wed, 20 Dec 2023 20:15:46 GMT  
		Size: 27.4 KB (27443 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.17-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:f586d56ed9d02567fdfdd67f08f9ab2315712f70cd48fef6110622089b57d0b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5398802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae6ab490260d7f4d0cfb1a495490606d1159a63dafe61fccb42c9b8b8bfb1567`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:e3eb0ea4f652282ad08228d0d146f33998b9e93641756d780ac0205aa828c070 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"dc47dbaeb1c0874b264d34ddfec40e7d2b814e7db48d144e12d5991c743ef5fcf780ecbab72324e562dd84bb9c0e4dd71d14850b20ceaf470c46f8fe7510275b *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c7d387f1f267ea360529df8d70b246f949e1afdb2317cdf84b028cda80a093d1`  
		Last Modified: Thu, 30 Nov 2023 23:20:17 GMT  
		Size: 3.4 MB (3391875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f08a2d63d17b8d0f97c0c58f2c0d2e0a53351c5855632b01aa592fd749c5a8c4`  
		Last Modified: Wed, 20 Dec 2023 21:25:07 GMT  
		Size: 2.0 MB (2003177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41a649664a957fb5fac9e84917d27c3fd6cd9457d5e1da4483479fc47a40814d`  
		Last Modified: Wed, 20 Dec 2023 21:25:06 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c2eeaa63a216e39c2e1bf1660ade8ea960067042cd88616286f7b83adaba7f9`  
		Last Modified: Wed, 20 Dec 2023 21:25:06 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65122cf84e61bda3effe490be3468427e8038bac4f55ff8f8f60b0eebc9433e`  
		Last Modified: Wed, 20 Dec 2023 21:25:06 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d141732d93e6bb476a2158a94778d5135f30596806041c85c53da49a88c9df`  
		Last Modified: Wed, 20 Dec 2023 21:25:08 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.17-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:95fc11d2814b34223eb55dca85bd879ef9f84d846a386b8d9a6adbf8398bdb03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.7 KB (725670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d880859e7260ce1969a80bb6ecce1a5ff06888893a78d090722c63e11cac6088`

```dockerfile
```

-	Layers:
	-	`sha256:a9c0e2b1a0282baee12f13f102e596cfeb9b9d441484a8e94fb3c0c48b7bf479`  
		Last Modified: Wed, 20 Dec 2023 21:25:06 GMT  
		Size: 698.1 KB (698090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38bd87fd52493897ec4847eabcf90c003a6330ebfbd9530079b33abbe90d83f5`  
		Last Modified: Wed, 20 Dec 2023 21:25:06 GMT  
		Size: 27.6 KB (27580 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.17-slim` - linux; s390x

```console
$ docker pull nginx@sha256:762af164d40468c06e03b417674070a4f3572e1d1b0d6b9db3307d93a24ddff0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5014163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2be2c08a0c40120c5bcf73a27986320d663e486d1a3c1f8a3d3e11c6c54a629`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:bf416048d22b9a0deecb508385355d79b8d5d12b655c600dbdc0948f7dcbb2c2 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"dc47dbaeb1c0874b264d34ddfec40e7d2b814e7db48d144e12d5991c743ef5fcf780ecbab72324e562dd84bb9c0e4dd71d14850b20ceaf470c46f8fe7510275b *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7e9e7e53b618240d2e82e8cab6b677eab6786c4210dcc2b1a35bfd4cb492757e`  
		Last Modified: Thu, 30 Nov 2023 22:43:01 GMT  
		Size: 3.2 MB (3176332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3874ae5a9f033f4f35d9cc75926793f942924e57022f90cf215545ede16a3bbc`  
		Last Modified: Wed, 20 Dec 2023 21:30:32 GMT  
		Size: 1.8 MB (1834078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd478a7b185bfcbc763484727cc5112a12a848eb6cf531c23a64bee9a0f8378f`  
		Last Modified: Wed, 20 Dec 2023 21:30:32 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6464e6839ada80df440048c45fe281b5b404053003131502d6eb89824ef95b32`  
		Last Modified: Wed, 20 Dec 2023 21:30:32 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf39b1c8443c0858b86d3acc5ce37fee14f7847d9432951026b39ad5878f3af2`  
		Last Modified: Wed, 20 Dec 2023 21:30:32 GMT  
		Size: 770.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0440972494612fda37d82f53f01f2b0739f20409934f4c97bd2dbfcd7e7a76db`  
		Last Modified: Wed, 20 Dec 2023 21:30:33 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.17-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8381a86febac911884282753f08125427e04e8c256593cc48289566edb38acdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **725.6 KB (725575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbb117640e681640aa9157d3b4190da64fa03217a1a1a3d910670a0c9b0b46f9`

```dockerfile
```

-	Layers:
	-	`sha256:77e619999bd354b8fd93d3cd2054a634b53339caa1690574f1d2100c47e69698`  
		Last Modified: Wed, 20 Dec 2023 21:30:32 GMT  
		Size: 698.0 KB (698044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8630fcf76f54118ab3ab2e6c63f4a9433807cdec1d828165a5129a34c3314061`  
		Last Modified: Wed, 20 Dec 2023 21:30:32 GMT  
		Size: 27.5 KB (27531 bytes)  
		MIME: application/vnd.in-toto+json
