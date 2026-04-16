## `nginx:stable-alpine3.23-slim`

```console
$ docker pull nginx@sha256:6eefb45c9ba67b69d9604b38b22d128f589ed9523c3e02e47cebbde96ad891bf
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
$ docker pull nginx@sha256:860794b0d073ec1abd9815b88979f415a402bd02de97e37c14df1976e34fe59d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5739681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9414817d1de7cf4df21eecce305dde69e08cdd8699f546f502a83ed129fedefb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 20:17:53 GMT
ENV NGINX_VERSION=1.30.0
# Wed, 15 Apr 2026 20:17:53 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 20:17:53 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 20:17:53 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:17:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:17:53 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:17:53 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:17:53 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f175ecb4aec16f58caab168a3b44751c86cba01f05e4cc66b618a8fe3e6f7c7`  
		Last Modified: Wed, 15 Apr 2026 20:17:59 GMT  
		Size: 1.9 MB (1870903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57f9500efd55884217ce5c4eff9d51c96b86fdbb2c2c8d9472573e52f33225b`  
		Last Modified: Wed, 15 Apr 2026 20:17:59 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15c316802cf5c3cf4320e85a73f67b903364a6cc459445769d294c3c7cdf5007`  
		Last Modified: Wed, 15 Apr 2026 20:17:58 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294d7581acec76bb5afaf68b7492deefd69065dd564ee81f5ffda7cbda699a70`  
		Last Modified: Wed, 15 Apr 2026 20:17:59 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b087412f0732e4526aeca7fed15f7dfc458e114e9ac81705390f52119d85b943`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:409c3fbf3b04f3111c7cc04c594031e36bedff3a262da6628eed92e15621cf2c`  
		Last Modified: Wed, 15 Apr 2026 20:18:00 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:92be15cbc9e96077e1e14ea64be478636307c14892a2f21466f750916bdb79b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.0 KB (503045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff84c4014153540144a71094d9985b4e3d73602ae0ed1d31663c5486a7533c3b`

```dockerfile
```

-	Layers:
	-	`sha256:84ed6c64abfc0996e00d263d385fdbd40fc15ed43458d6bd362f2a6170b0091c`  
		Last Modified: Wed, 15 Apr 2026 20:17:59 GMT  
		Size: 472.8 KB (472756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea29cd247ddbf4d685fe35dc87aa0e9a369b9b428cf9360ee0ac03b3030e845d`  
		Last Modified: Wed, 15 Apr 2026 20:17:58 GMT  
		Size: 30.3 KB (30289 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:090bf1100a3494981527bc2566a0099e8665c022ba93057398e41e7223ff9a63
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49aeb0f17ef649d833d36503a45fd9ada1ff50ebbdfaffa3c5484c8b6c4c53e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 20:19:08 GMT
ENV NGINX_VERSION=1.30.0
# Wed, 15 Apr 2026 20:19:08 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 20:19:08 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 20:19:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:19:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:19:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:19:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:19:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025f5f7d46d2119b6643d92cc40869f7602c714637c2f457ab77651ae6e021b6`  
		Last Modified: Wed, 15 Apr 2026 20:19:12 GMT  
		Size: 1.9 MB (1868546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ee7bd4c0129258f5ddc07c9a55b23c8b68fb2c52bf960fbf378a4fd22d4686`  
		Last Modified: Wed, 15 Apr 2026 20:19:11 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73546a75e885ed06339ebcf7260514b3d9b588f86f04a17b630026ef34bcac93`  
		Last Modified: Wed, 15 Apr 2026 20:19:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5305fa431d3729c1fa2e21cda5bcf5ecafee8edfa8b88f4688a8e1b871f20be`  
		Last Modified: Wed, 15 Apr 2026 20:19:12 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:046ff4d4b7808a67a7756c15ecc4fe366769a24093d5e4224c7a8bcb2b99c99c`  
		Last Modified: Wed, 15 Apr 2026 20:19:13 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458416acfc513d38a9c1a7d255d9f53bd17357605180f2703c93a8c1ca619873`  
		Last Modified: Wed, 15 Apr 2026 20:19:13 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:f4bad2c88d17ecd1ce74ec48b2d08404b170f73528f370b8d4755efd42216951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc83a8501ea13dbd778abe1369040283d0ac77c916e64a61cf5dd42d12f7a3b0`

```dockerfile
```

-	Layers:
	-	`sha256:ee4cf0ab6bedbdca16b916588271fddd5341f0d480a94ad22ebbdb43234980b3`  
		Last Modified: Wed, 15 Apr 2026 20:19:11 GMT  
		Size: 30.2 KB (30170 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:18b9e970e20aa05804be75f7cf9993db30d1408eda3b4727bf48d1d0e47bae39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4981569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ed99a1e330b5b6f4c7b850bd53d2cf5aa059b440cb9b1db4f1c428681d0c313`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:19:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 20:19:16 GMT
ENV NGINX_VERSION=1.30.0
# Wed, 15 Apr 2026 20:19:16 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 20:19:16 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 20:19:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:19:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:19:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:19:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:19:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd84e3fa292073d2248a7cc76ae3eea9cabdcb83e2bf199ccf53b1ad83e8efe2`  
		Last Modified: Wed, 15 Apr 2026 20:19:21 GMT  
		Size: 1.7 MB (1693849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d4fb0ae27ea25f527f4d387a0c0162e9320aeb1d11c1f1cf09518e8116d6ae9`  
		Last Modified: Wed, 15 Apr 2026 20:19:21 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3773fd9a1c510478b8cae2edf7dd22f3bc5b57f3d16fb9eb046538947812e2c`  
		Last Modified: Wed, 15 Apr 2026 20:19:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25e6b7502f09ef7c4a5fd81a8bd0203aadfdab8ca89082924998a2858d038c85`  
		Last Modified: Wed, 15 Apr 2026 20:19:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae295f4a3b5962a7e2e803227d03ad7de682d5696f57ab4944f93c089b616a5d`  
		Last Modified: Wed, 15 Apr 2026 20:19:22 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9695942fa6aa2036bc4b0626c2712d633538b6136dc4a8819ee9db6900df130e`  
		Last Modified: Wed, 15 Apr 2026 20:19:22 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:deecf036afa5070b44f0fa266a8b770d46ccd5d9a3922223ad1e57fd1c0fcf57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf6a0fc58a31ae1f007c6f9629e0caec25c1e420ad62105be7cf0c3258e62afc`

```dockerfile
```

-	Layers:
	-	`sha256:cb5141ac8cefc6dc45ff7ff44976a5cc6fc9b5affbbc75548c0a9726e400af9e`  
		Last Modified: Wed, 15 Apr 2026 20:19:21 GMT  
		Size: 472.2 KB (472158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a5c66c7f2ba42e14c4c9a4c5d2bea60a72317aa19112cf29018c8663da45309`  
		Last Modified: Wed, 15 Apr 2026 20:19:21 GMT  
		Size: 30.4 KB (30385 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:7183112f4f43c872b0c0a18d34adbb84fc350b41bc96c4ac55d59d7353317b85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6095849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a76012d80d5e34393a0a5e32d9150a4f1212808dc43749c90df6804ff97c568`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 20:16:22 GMT
ENV NGINX_VERSION=1.30.0
# Wed, 15 Apr 2026 20:16:22 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 20:16:22 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 20:16:22 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:16:22 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:16:22 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d507f9381a1dd83d4a1a66ac3139c87fb1e12f884a13a0319bcd27626eb39e4c`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 1.9 MB (1891388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efa9a2f6e090eb0b8cea1ea8233c46430f52c6b25aed22b6214fb284836ebc85`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:468ad5067d83ad01404cc2ed5ba59e9cdbbd8043c83966413522bca408fa7fcd`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a618d92477fb39ae68709b70130b862f7fc3ccc6ceb5d790f8461b3afbf0bce`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a385948d96b6b270a5baedaf681be973e87317d3704400208db0f6d87c4cebfe`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3311c3f0e5fa73e300119a0d475b021723e11698467fc8f38ab26365b3c2583`  
		Last Modified: Wed, 15 Apr 2026 20:16:29 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:f1324bd21c597fb84baa1bac432e6e71d630373c78ea389c2f354deb04c9e145
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.6 KB (502603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16dbeec0a21d2cc4ec9bb473d4e7313f53e6b14cf1a148802e83fa41b7143373`

```dockerfile
```

-	Layers:
	-	`sha256:70aae29ecdb36a08f5e0a5eb18e736be20bb38aea7fbe7ab4afe322df04780a6`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 472.2 KB (472186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cf1ab4d10141c23fc8a6ca6a21f86dc39cc3f0d640957210494ade518a8101fb`  
		Last Modified: Wed, 15 Apr 2026 20:16:28 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; 386

```console
$ docker pull nginx@sha256:f9ccafde45bbff27d4e533ea3dbf5a2e0a7d3c86167d2672f69287b4ede531fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8388943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37efb99ba24c93126f99d20a32a61a7bc9446cb27925d7c2a3b038fc73a9bb6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 14 Apr 2026 23:12:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 14 Apr 2026 23:12:45 GMT
ENV NGINX_VERSION=1.30.0
# Tue, 14 Apr 2026 23:12:45 GMT
ENV PKG_RELEASE=1
# Tue, 14 Apr 2026 23:12:45 GMT
ENV DYNPKG_RELEASE=1
# Tue, 14 Apr 2026 23:12:45 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 14 Apr 2026 23:12:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 14 Apr 2026 23:12:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 14 Apr 2026 23:12:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 14 Apr 2026 23:12:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 14 Apr 2026 23:12:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 14 Apr 2026 23:12:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 14 Apr 2026 23:12:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 14 Apr 2026 23:12:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 14 Apr 2026 23:12:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21a600373ad4feb62d62a2f6ed34e47ce2d7ce2deb69ffe91fab4c5884505c5f`  
		Last Modified: Tue, 14 Apr 2026 23:12:50 GMT  
		Size: 4.7 MB (4697355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd8c53debec207b5be9d837b10a62bc8611c6f30b7ffbef01c3f737eeb5ce59`  
		Last Modified: Tue, 14 Apr 2026 23:12:50 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8a4fba4e55249cc03b2d35c54bff8082505d8d98961c13817704460faa8278`  
		Last Modified: Tue, 14 Apr 2026 23:12:50 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20adc99947e77c4c65658f200c0916df6d9507b403761f5dc80368aedd815da3`  
		Last Modified: Tue, 14 Apr 2026 23:12:50 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebb858f1c1184171db24fef0d2e47d7e49b9ec195871fc9bd90582291e24e2a1`  
		Last Modified: Tue, 14 Apr 2026 23:12:51 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc22906ce26f28a3c0e03ae71d6cc6fb01f4e2d23c1e1c80b48409c272530b9d`  
		Last Modified: Tue, 14 Apr 2026 23:12:51 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:afd6ebb2ae9c63d2738427b84b688d64d1dc8fe069deed2d2c622252a22c21c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.0 KB (503963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02bc84b4c934cfe09e9dd8707a0d50af69fc91130a3d4be17dfd24ee92932cb6`

```dockerfile
```

-	Layers:
	-	`sha256:ab1282eb6c9feea3c33838d9d23a490f92c84de1799d5ec36002abd209806c4b`  
		Last Modified: Tue, 14 Apr 2026 23:12:50 GMT  
		Size: 473.7 KB (473716 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4eedbaed4a7fc406e451bab310d98d44d58c6eee920f428f202a67b75059883`  
		Last Modified: Tue, 14 Apr 2026 23:12:50 GMT  
		Size: 30.2 KB (30247 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:00f27542cd71c89ec95412b3f5d1885b7352efddda6d91b05eb4e8639ea971d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5799051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0e0d6379fb358e754bb6a5de0f527849d0d5b4458e0ff61ba950c5e74d939e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:20:38 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 20:20:38 GMT
ENV NGINX_VERSION=1.30.0
# Wed, 15 Apr 2026 20:20:38 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 20:20:38 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 20:20:38 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:20:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:20:38 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:20:39 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:20:39 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:20:39 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:20:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:20:39 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:20:39 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:20:39 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:909a15fc229be609a654a593fead97bf343625c842e0ea0cc56805c75633b843`  
		Last Modified: Wed, 15 Apr 2026 20:20:50 GMT  
		Size: 2.0 MB (1963521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd86d5796ecff5402cfb0663b6960dbc70a1bb9ad36b8df84f730289f523d97d`  
		Last Modified: Wed, 15 Apr 2026 20:20:50 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b08c210e03c637c82f693346102a1ac707124b9fffdf32d2889e642419dba2`  
		Last Modified: Wed, 15 Apr 2026 20:20:50 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e67a3b25763cb061bec44bdd39ec744eec9da71b7494b3fa7f1dd67f65d6a2c`  
		Last Modified: Wed, 15 Apr 2026 20:20:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5db8086c5a713413680420bafd18f56aa083457e9b0790f1e87c0c3ef66131`  
		Last Modified: Wed, 15 Apr 2026 20:20:51 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:622bd011ac02534c7b4e2f7e775aab6d01705cb5b0fe90d338827aa213ea890d`  
		Last Modified: Wed, 15 Apr 2026 20:20:51 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:796abbab6e5895bfd4e407bee04fdef0abf5a826e4245e3d106e3fc24acf41eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b89a11f8758aaf13976d80bfcaa9b036d251cf5ee717020574f2d9a86be9feca`

```dockerfile
```

-	Layers:
	-	`sha256:f210fee8dc8725fb1a7aa089424ca98308376695e1b7d86e275d56724bae1fc8`  
		Last Modified: Wed, 15 Apr 2026 20:20:50 GMT  
		Size: 472.2 KB (472151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:865bcdacb850817f77cb6e4cdff95f0bd33416615d08989c248c88b915dec281`  
		Last Modified: Wed, 15 Apr 2026 20:20:50 GMT  
		Size: 30.3 KB (30345 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:c75f3acae754705237cef156a2c8a8a87b864dd49febea79a17fb614a0be7f7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8128156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f4f8a5526c169c813e2a02e8006b8baabcb31d3b9ed6038af821e0dc6e013d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 02:14:54 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 02:14:54 GMT
ENV NGINX_VERSION=1.30.0
# Wed, 15 Apr 2026 02:14:54 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 02:14:54 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 02:14:54 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 02:14:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 02:14:54 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 02:14:54 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 02:14:54 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 02:14:54 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 02:14:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 02:14:54 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 02:14:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 02:14:54 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bcbf6e73c4e756b32e8c6150452f0fe15bfa911c4ecbc8d5ebdf68e916c1db7`  
		Last Modified: Wed, 15 Apr 2026 02:15:30 GMT  
		Size: 4.5 MB (4538264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ec575ed72affdd7ab96cfce94da64093c3cd228b7a3e8ac4ee19b4441a3c3d6`  
		Last Modified: Wed, 15 Apr 2026 02:15:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20cfb2bb4b3745d134316d8da1239ee618709b404f5ea1622eae6e8bcdf28080`  
		Last Modified: Wed, 15 Apr 2026 02:15:30 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ee6c77797a90c6d40feb313fbffe9309af1f03ed309590fbd284b245627d775`  
		Last Modified: Wed, 15 Apr 2026 02:15:30 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87ff97c0446686bfb78fdfcb83d7a6078db2789cc7be3c380e686d9bb7ac9f89`  
		Last Modified: Wed, 15 Apr 2026 02:15:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d8e61aeeff7e17464e47251ef0db9f0758c363953b132d1d97a8d8ff4c67b9c`  
		Last Modified: Wed, 15 Apr 2026 02:15:31 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:bbadfd102db6888c838f437927f639b4d6ebc38282dc14b57ee8bc0af3cb05e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.5 KB (503487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80ed92ce2ed657f5e7c0962eda87a8c7b54820a9b726ffdc6871a29fa5aaf51e`

```dockerfile
```

-	Layers:
	-	`sha256:465a7cee3f1281ac10b26dd22cbd3246ac00f9c77868f452e9bf6b3b2c6b15b1`  
		Last Modified: Wed, 15 Apr 2026 02:15:30 GMT  
		Size: 473.1 KB (473142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63cb032e20951019ca45ceb7d90ea4db69e54679464b50cdcc669951110cbdd6`  
		Last Modified: Wed, 15 Apr 2026 02:15:29 GMT  
		Size: 30.3 KB (30345 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-slim` - linux; s390x

```console
$ docker pull nginx@sha256:972f545b0435262c307e4ef641bea83eff2ea7a5168f4409ef9f789dd37ed944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5721019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447510112b8cff9de040de79456b3434eb0fb09c7a19ac80ec378467927a6c57`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:16:36 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 15 Apr 2026 20:16:36 GMT
ENV NGINX_VERSION=1.30.0
# Wed, 15 Apr 2026 20:16:36 GMT
ENV PKG_RELEASE=1
# Wed, 15 Apr 2026 20:16:36 GMT
ENV DYNPKG_RELEASE=1
# Wed, 15 Apr 2026 20:16:36 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 15 Apr 2026 20:16:36 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:36 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:36 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:36 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 15 Apr 2026 20:16:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 15 Apr 2026 20:16:36 GMT
EXPOSE map[80/tcp:{}]
# Wed, 15 Apr 2026 20:16:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 15 Apr 2026 20:16:36 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c19bfbdc65f80ad1a30296d8c3063b99005f43d1813b01a3db4e28e98a0504`  
		Last Modified: Wed, 15 Apr 2026 20:16:46 GMT  
		Size: 2.0 MB (1989883 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55ee362c11ce56d5a58d07fb18c536a93cdac5c2ac35438a1d05a20d4773cc22`  
		Last Modified: Wed, 15 Apr 2026 20:16:46 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d29422a967635c19f7a94919a70925be2fe358c82358f619ca88a29de3a3eb01`  
		Last Modified: Wed, 15 Apr 2026 20:16:45 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c875a7572a3c92917cb926a59100176c90fc7956e5225915b9c72765215cf3`  
		Last Modified: Wed, 15 Apr 2026 20:16:45 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56a6e14b5c72d02d2ce332762179396a65e9599dc01b17ef657520d47f199682`  
		Last Modified: Wed, 15 Apr 2026 20:16:47 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc3335b6990963b0af730533539aa6cfda950412458515a8e22225ce3dc49f6`  
		Last Modified: Wed, 15 Apr 2026 20:16:47 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b959e969a4caff8bf7261efcf2456d3a80e9eb8b8e5492350e2e672b461157ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502394 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4197b32bc2df9427f5c4a425309bd19b829fce35e6881f1366389affc6e98b9f`

```dockerfile
```

-	Layers:
	-	`sha256:3f62c69b1d3806667f65cf8a3279d650c226a28e906b85aa0accb34122393678`  
		Last Modified: Wed, 15 Apr 2026 20:16:45 GMT  
		Size: 472.1 KB (472105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:966d69e5ed031a4652ebeb15c9bc5a4b97eae5cd32959d47a93b40964ae7a740`  
		Last Modified: Wed, 15 Apr 2026 20:16:45 GMT  
		Size: 30.3 KB (30289 bytes)  
		MIME: application/vnd.in-toto+json
