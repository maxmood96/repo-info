## `nginx:alpine3.23-slim`

```console
$ docker pull nginx@sha256:727be5c07183e41885a7ddeb069ca4cc540133493afe24b9eebd931bbbb02e79
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

### `nginx:alpine3.23-slim` - linux; amd64

```console
$ docker pull nginx@sha256:60291ef4f8ca787769782870aa6d14474ff41a200f9f5c697305c406732eddfd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc447918bc68822745b9c0fff90edd6d509ae07902119589c5a677d00e3e56c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:15:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:15:09 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:15:09 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:15:09 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:15:09 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && PKGOSSCHECKSUM=\"8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz\"                 && if [ \"\$(openssl sha512 -r 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && cd pkg-oss-9d879d57ef75661eaed35e787ef434b2f85771f6                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:15:09 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:15:09 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:15:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:15:09 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e661a44239bffc66a00e3a0d6c45af7059317a60a5685760937a68d0b3b624`  
		Last Modified: Tue, 19 May 2026 20:15:15 GMT  
		Size: 1.9 MB (1882821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c084cd9252c2e4b305bd605f0b6534943993f25adfbc92dec27d9f2dcca45a2`  
		Last Modified: Tue, 19 May 2026 20:15:15 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04a7ff7b108a8f7d67888aa7f32283bcda09520660a1d149bd4e6a294cf8b135`  
		Last Modified: Tue, 19 May 2026 20:15:15 GMT  
		Size: 951.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcace0045394f92e9a583eb4f11a674f91cc91d407b85d52afe3f6209672ca1e`  
		Last Modified: Tue, 19 May 2026 20:15:15 GMT  
		Size: 400.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e0029eccff957b151ddd0fb727628e9ae5fcde85cb9771e74d471efe031245`  
		Last Modified: Tue, 19 May 2026 20:15:16 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0faf356544319b35bb9aa03595e556e22277228565e7470fa7da4b1a2c999aa5`  
		Last Modified: Tue, 19 May 2026 20:15:17 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:d731b520730b37aaa28f5e7452c645fb48d42c0252742b67ee1f103a0a80d86f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.7 KB (505710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c27c62785b2a66496256d56c3ff8460f7d634c3107ebcd74d754c238de60e8e`

```dockerfile
```

-	Layers:
	-	`sha256:6237b6a5da2de43113bac330b307579825a5443b72455536d16663e26578a297`  
		Last Modified: Tue, 19 May 2026 20:15:15 GMT  
		Size: 474.0 KB (474012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1170bdf25b9d60b1b6f0ff93f1ad1591833242806e31206c9fde3c69f51a2dd8`  
		Last Modified: Tue, 19 May 2026 20:15:15 GMT  
		Size: 31.7 KB (31698 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:c7fcd667c7cc27d832ea03608612bea13413e702a485680cd5207f040980f77c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13a8194826137d10d24bf09a94b5c9c4d5908b592713c86b3e9c9574d639ad8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:14:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:14:45 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:14:45 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:14:45 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:14:45 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && PKGOSSCHECKSUM=\"8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz\"                 && if [ \"\$(openssl sha512 -r 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && cd pkg-oss-9d879d57ef75661eaed35e787ef434b2f85771f6                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:14:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:14:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:14:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:14:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1505b94035af93605e05006251a2b38bea81b1270efab0332689349431c81f1`  
		Last Modified: Tue, 19 May 2026 20:14:50 GMT  
		Size: 1.9 MB (1883287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceb9685b19e1b78b990034ab3cdafadd2900f15ef20d98d4973afb10b4bffad`  
		Last Modified: Tue, 19 May 2026 20:14:50 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a3e8b3402180c581ef5d8f1fa6d84aa53e20981f728562313237306e9f1571`  
		Last Modified: Tue, 19 May 2026 20:14:49 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3b8f2bbc1ebc1db8b149f6ea44f49c8184895b37c6a16856b58137638deff5e`  
		Last Modified: Tue, 19 May 2026 20:14:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbdee355e9c13a1af2d6cdfae724d670ee368790e3277cc487896dfc3c6d38a2`  
		Last Modified: Tue, 19 May 2026 20:14:51 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a7f24af2ae8c6f91b45d49082c058812876201b4eea194bd7aee8cbe2fb5db`  
		Last Modified: Tue, 19 May 2026 20:14:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:2a1d88d46d268d01d1fb0c04f3775cd26d16445c8d65ce1ccd42079bceb49ffc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31611 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58c8faaee5e44daf9bc823a5dbe4718ce4424562ede28c15c7f3ba4fec209d3b`

```dockerfile
```

-	Layers:
	-	`sha256:b1db4700012e019a3b53ad2620e0958bce4438cbe265e4e2a65cadebf4dfda01`  
		Last Modified: Tue, 19 May 2026 20:14:50 GMT  
		Size: 31.6 KB (31611 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:546690d62e2ef4829099a7d8b69e1939adb7585a222b99e607c77aa299705599
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996065 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c59bbf2fff1c830b8cb52b72a03cbffddf3a5ae75564700d6c37f7dc5a44ddea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:15:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:15:24 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:15:24 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:15:24 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:15:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && PKGOSSCHECKSUM=\"8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz\"                 && if [ \"\$(openssl sha512 -r 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && cd pkg-oss-9d879d57ef75661eaed35e787ef434b2f85771f6                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:15:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:15:24 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:15:24 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:15:24 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8043ae853de01bf51d9bfbb28a5db58b39c7abcf48fdb9e07afa5d80cba38f2`  
		Last Modified: Tue, 19 May 2026 20:15:29 GMT  
		Size: 1.7 MB (1708350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1af29098d817a16823c2a87197fcd3c5e1f8915912a1e7182cb6ca4b1037d9b`  
		Last Modified: Tue, 19 May 2026 20:15:29 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a17f7675daad2f96c770a16a69cff6423b1b267ac03273149e974ba4d2344df6`  
		Last Modified: Tue, 19 May 2026 20:15:29 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb821db83e7094e0e5f0c29fcad97858063aac8222dda26c633904b57a4c972`  
		Last Modified: Tue, 19 May 2026 20:15:29 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f88fa478c2de65f6c37a61b9a7cc25b1595b3c49eff9a084477fbf51b9494b6`  
		Last Modified: Tue, 19 May 2026 20:15:30 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba99f27e36eed4bcd9045bd9ed0e9030a4183e483a009a3710a5b440c5de1fa`  
		Last Modified: Tue, 19 May 2026 20:15:30 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:5a9d0bcd1f6f348a1dc6959aee3da984da8290a8d52b5a877c658eb7b5d8fa09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.3 KB (505272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:606c2eaba2e102573720dcf827583d85bc5b3f0749f83c92730dd099b4bd267a`

```dockerfile
```

-	Layers:
	-	`sha256:201f641e26188400499a1fa827e58a8b2b1d307bf062365bf911a6f964d7b4b5`  
		Last Modified: Tue, 19 May 2026 20:15:29 GMT  
		Size: 473.4 KB (473446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ad74ecda3a126eee100a15fb685d010bcf3a44ffb59dec1e2482103813cbea0`  
		Last Modified: Tue, 19 May 2026 20:15:29 GMT  
		Size: 31.8 KB (31826 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:9df43d3fad7b92b09c4ee2bfe3eb50bad07e36d98a5d25a3912c65353b1d0f92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6105716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c904d4a38a062a96aa5baccacf0dcbe36989922b4499bf23b59b92d0e0937fe0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:13:23 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:13:23 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:13:23 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:13:23 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:13:23 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && PKGOSSCHECKSUM=\"8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz\"                 && if [ \"\$(openssl sha512 -r 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && cd pkg-oss-9d879d57ef75661eaed35e787ef434b2f85771f6                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:13:23 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:23 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:23 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:23 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:13:23 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:13:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:13:23 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba38a4c675f49838286ecfb59fcb582506c548d46f1864da7fe230d282c45a81`  
		Last Modified: Tue, 19 May 2026 20:13:28 GMT  
		Size: 1.9 MB (1901252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff3cfc9ab5b15555fdb0054c401fc2ff8f886d533de9c1a501ddc47a6391d0f9`  
		Last Modified: Tue, 19 May 2026 20:13:28 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacb12de73373bc23020bd7939a9c86f4ecc6fbab43b2217db081d6b0a9f1a6c`  
		Last Modified: Tue, 19 May 2026 20:13:28 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27e0911c57b99e24e4bc736ed02a66317c7173f85c9cff2a8a9ceeefa3c9979c`  
		Last Modified: Tue, 19 May 2026 20:13:28 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0690d37582b483d582f105f2d97999b6aebb21770aeabcd6a4b73c3e99f605e8`  
		Last Modified: Tue, 19 May 2026 20:13:29 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:066eb4b111606d3564cb485edbfd9faee6505c4fdf0c59e6e77db2bed8d0d930`  
		Last Modified: Tue, 19 May 2026 20:13:29 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:32b47256c72f1d66556707999d0a152da9ce22c030d4b190a143a4c82edc3f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.4 KB (505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2382630e0686d9f772173604216fecc491e86b8c0b8ecbaea9b9cb8fd9c8beed`

```dockerfile
```

-	Layers:
	-	`sha256:c72988814a16552981e3731c4468749f88eff42150d3a5165151ca66a93c4339`  
		Last Modified: Tue, 19 May 2026 20:13:28 GMT  
		Size: 473.5 KB (473490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2577d56a85aae65ed8a8ea4a14c29e0dab35b0ed2dbc73c4de4863e4a70859da`  
		Last Modified: Tue, 19 May 2026 20:13:28 GMT  
		Size: 31.9 KB (31874 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; 386

```console
$ docker pull nginx@sha256:53af279e6a2d4e906c27c2a6324ce5230090b414907f0a66b980457f5dcf2488
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d955d8360f2a6c8ec9835854d0bcc5a41783f39fc9ca3f2ca6b28480f4f310`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:16:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:16:05 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:16:05 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:16:05 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:16:05 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && PKGOSSCHECKSUM=\"8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz\"                 && if [ \"\$(openssl sha512 -r 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && cd pkg-oss-9d879d57ef75661eaed35e787ef434b2f85771f6                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:16:05 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:05 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:05 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:05 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:16:05 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:16:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:16:05 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d4fcfb5cc56fb8c14422f98c4b53c621e8e921c5c1050be9894330a70795330`  
		Last Modified: Tue, 19 May 2026 20:16:11 GMT  
		Size: 2.0 MB (1955278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16463197f6bcbc2f1c844a133b3145aca43fd170644c4e839cd2dfe3688e6da9`  
		Last Modified: Tue, 19 May 2026 20:16:11 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b460cbad65cf3dbbaeff55df5ae12ac6a84eb25d103816f08ac5edcaabd5dec7`  
		Last Modified: Tue, 19 May 2026 20:16:11 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbc0a2a833f4bdd030f6c850fe590ef0f2c3f9ab210a96fb30352a3f1b0ef42e`  
		Last Modified: Tue, 19 May 2026 20:16:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4334d5949392da53a4dd5796ba07f69c88789135305c70dccdab3e0ff4c63c4a`  
		Last Modified: Tue, 19 May 2026 20:16:12 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0276e01dca0f3f3289569cd9aa7569894b850cab5a6c446da386cb918cbaf3da`  
		Last Modified: Tue, 19 May 2026 20:16:12 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3f56b97a25d5f20c90a90b43587674132cd349524b2d3bb6a84799499edd1d8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.6 KB (505593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16d9810a9a6b178af85e21bb393f215aaf071ad3a96f692b41204149aef52226`

```dockerfile
```

-	Layers:
	-	`sha256:2d9aa23a6863edd85cb1e344d2f6b8c82a48accc8062edbd3425f98984b830a9`  
		Last Modified: Tue, 19 May 2026 20:16:11 GMT  
		Size: 474.0 KB (473957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea4e7572d06b6300bc1961685ea0c038368e9deb8b46edc0efbf56eda10de0f9`  
		Last Modified: Tue, 19 May 2026 20:16:11 GMT  
		Size: 31.6 KB (31636 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:33aca75b1daf0284bda5259649c79591cb73fc1a30e81cc095457f86bf4c7f75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c50dc49cd6290b785ba70efff1274d96593ddb84c235003a16069268b0d568d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:13:54 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:13:54 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:13:54 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:13:54 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:13:54 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && PKGOSSCHECKSUM=\"8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz\"                 && if [ \"\$(openssl sha512 -r 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && cd pkg-oss-9d879d57ef75661eaed35e787ef434b2f85771f6                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:55 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:13:55 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:56 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:56 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:56 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:13:56 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:13:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:13:56 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7aff0673fbcec9ad9712107691e00bc893092e643137feffaf1ddb4a75c8841`  
		Last Modified: Tue, 19 May 2026 20:14:16 GMT  
		Size: 2.0 MB (1975157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7554d6f1fedbef541fb071e89eff2d36af9993d5215a674f5224135635674aa6`  
		Last Modified: Tue, 19 May 2026 20:14:15 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a16d9b875938cc516e4fead321cb59589dfd0c828799f9d96edd1a6e1c86d34d`  
		Last Modified: Tue, 19 May 2026 20:14:15 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5d844bcb8396c77f78eb47a78b6d84aef607ce60aca6d04537356633a444a4`  
		Last Modified: Tue, 19 May 2026 20:14:15 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1278cd57fee86ec0e9dc85af32c376c15ccf76ec7d236c0f66b73b2c10524c67`  
		Last Modified: Tue, 19 May 2026 20:14:16 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a970fc6ddb6489b1e79138648c6a5b3a265ee82a5398a2cfb5c860e66194616e`  
		Last Modified: Tue, 19 May 2026 20:14:16 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:efdad76dff26320ba08f02de5593b6b8fe09e6fa3ce22da505643d75afae8001
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.2 KB (505209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37b1ff3ebb09e85c02ebbf6a26d3d707b6d7305e41f16baeed746b227ed7584`

```dockerfile
```

-	Layers:
	-	`sha256:05b6329b56733c8777a7fdcdc6d80e3c2c5fea35710376ac58556728b8b0ca67`  
		Last Modified: Tue, 19 May 2026 20:14:15 GMT  
		Size: 473.4 KB (473431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec63506d675decdc68d8709f7b96d34d63f7427063ec97bc96494990fe5994ef`  
		Last Modified: Tue, 19 May 2026 20:14:16 GMT  
		Size: 31.8 KB (31778 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:91febda531fcfe3b8a445bb9872eb49a9293dc189063e01c402afee6a90d107b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5521538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891419739b88790e00f8b83de86ec164f07229aaf0abe69113c6e0787220d5b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 06:54:15 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 14 May 2026 06:54:15 GMT
ENV NGINX_VERSION=1.31.0
# Thu, 14 May 2026 06:54:15 GMT
ENV PKG_RELEASE=1
# Thu, 14 May 2026 06:54:15 GMT
ENV DYNPKG_RELEASE=1
# Thu, 14 May 2026 06:54:15 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"7c1dddf7d510642b6f352a16e4c8d7696c791a042cf9758282498d8bc8ae0760263874fbcbbadc420129b15701b32c50cebdc432ad9d2adb9776600b42cfb149 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:54:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 May 2026 06:54:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:54:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:54:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:54:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:54:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 May 2026 06:54:16 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 06:54:16 GMT
STOPSIGNAL SIGQUIT
# Thu, 14 May 2026 06:54:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:721a3717d9142f1bdca2edc17215925bc105a8f65310d95d03300d5e7c02c76e`  
		Last Modified: Thu, 14 May 2026 06:54:41 GMT  
		Size: 1.9 MB (1929273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29f0a9b9da4b7784b0336ea69f3ed94505100f19e8aa362763ad0740db697568`  
		Last Modified: Thu, 14 May 2026 06:54:41 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2afab4bb86beab604522121731bcdc8479124a912d8ae72105d486532d4dd371`  
		Last Modified: Thu, 14 May 2026 06:54:41 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc28fea6c0baac9f97955f87fa93892059a1504866beac866475c2d84d229f00`  
		Last Modified: Thu, 14 May 2026 06:54:41 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caa40ecf7b4734604e6fc1c45576d80f569ada2681ba56706a2c80370a730281`  
		Last Modified: Thu, 14 May 2026 06:54:42 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c33acdc5f0ba0227a6ffc689a97d4254cc054caf6d4d7adda6267cb7671d743`  
		Last Modified: Thu, 14 May 2026 06:54:42 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:e4bf3d4f1d800a76cb237f36357fd6f5c978f4e0e8cda07eb03e9ec425657212
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 KB (505099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcf5eaff6a39869ca6cdda5be63476e31324ac89fed8ddd293732c29a1d3aa67`

```dockerfile
```

-	Layers:
	-	`sha256:2970f06a933196882a7a6c4f504b57c4fda92118909387dc549cc3d4cd48ccc7`  
		Last Modified: Thu, 14 May 2026 06:54:41 GMT  
		Size: 473.4 KB (473427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efeff3b87f6e397c0d82b9733ce8d2fdda70508d38960ecce5367d32dbaeab4b`  
		Last Modified: Thu, 14 May 2026 06:54:41 GMT  
		Size: 31.7 KB (31672 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; s390x

```console
$ docker pull nginx@sha256:abe676237d0a84d9a356d13df35bab8e5199d45f4c36492826c3ec0e5f85fbf8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5734913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cabceb3f97b0ddd71d0cea71481b19a43b3992f5d269271f5f4e931b968325c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:14:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:14:19 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:14:19 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:14:19 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:14:19 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && PKGOSSCHECKSUM=\"8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz\"                 && if [ \"\$(openssl sha512 -r 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && cd pkg-oss-9d879d57ef75661eaed35e787ef434b2f85771f6                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:14:19 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:19 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:19 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:19 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:14:19 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:14:19 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:14:19 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1499527cb411072cb964457d4c258da21beb51622a8ab15420a2fed8b50e7aee`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 2.0 MB (2003787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ce9a3596e8f7cde3ccd6fe7e3d950f9b082d77a74f79ae1829fd56aab88969`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0328adf30446ae41d906a668ebad90feb5d64cf4483e892b8e493f37ed8184`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef4cd81eafc897fc5300bbb857a7961d7886bdfaf7613bbd4b679fd0c92d6f9`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290ac51623b7bcf950a2d8793e60f049f985f7127ce6ac2f36383c7a879cadf3`  
		Last Modified: Tue, 19 May 2026 20:14:31 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617bce522acee588c1f22cfc9ad96ec8579482411224aa589d57b01e0c3e2223`  
		Last Modified: Tue, 19 May 2026 20:14:31 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3aee23bf1b09c60c10888331a28a19f1f6dfde89824002fdd0751826c74f45b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 KB (505059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e5b1aa80c9b52abd0a7ffee3fd36981596eb35ad8bcc7864095347f693c975`

```dockerfile
```

-	Layers:
	-	`sha256:764ddde41c9c1ef1b192b9537c31c5d23f7e3b871e6bc81766d568a7a55f7441`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 473.4 KB (473361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05e7cc38177bbd389670eeb8833ff4434ee37f926f5fcbbcb4ecc9161843eb8b`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 31.7 KB (31698 bytes)  
		MIME: application/vnd.in-toto+json
