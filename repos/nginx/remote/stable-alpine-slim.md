## `nginx:stable-alpine-slim`

```console
$ docker pull nginx@sha256:2d9f7de595bc5967adb5b246c92730ac15dc9f8b4a29a610d7abae9c20650f35
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
$ docker pull nginx@sha256:7f6f5cfcf6772017eac393e40e218ea8e10a94509ba16368845d0aed01ed35d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.2 MB (8210012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d7aa0523777230e21506d3609c207a41e8da6680ee77aa128f462ca7a4833e3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 22:44:34 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:44:34 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:44:34 GMT
ENV PKG_RELEASE=1
# Wed, 17 Jun 2026 22:44:34 GMT
ENV DYNPKG_RELEASE=1
# Wed, 17 Jun 2026 22:44:34 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:44:34 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:34 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:34 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:34 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:44:34 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:44:34 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:44:34 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9202228ba081792c2c5ac4948e8bcd6ab8dba5dc924d1a3f4b55669e09ef8c2f`  
		Last Modified: Wed, 17 Jun 2026 22:44:39 GMT  
		Size: 4.3 MB (4341227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:351345d892fc7b2fbadb794798b984708e8f04d1a047033682db6733e768894f`  
		Last Modified: Wed, 17 Jun 2026 22:44:39 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f78b0907923e8fc2688e1e9837a130ff3e1862665529883caa90b6733462b6a8`  
		Last Modified: Wed, 17 Jun 2026 22:44:39 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8e31c2fbee2fdc2a76c16b6424345932e26b24f3e7320c4a116c998fb14e35`  
		Last Modified: Wed, 17 Jun 2026 22:44:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e92ed1188b45850a159bdb612cf901902878b6e897786b7d2c507204acf4ad3`  
		Last Modified: Wed, 17 Jun 2026 22:44:40 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e2f963d923464fe715a3d69e383c15d0231c40aae09d9e7f42cc5bc06fa6776`  
		Last Modified: Wed, 17 Jun 2026 22:44:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b4d321068d97335d33bb43fd5f3526de147d5ec87ea4f7abd6892b139602a5f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.0 KB (503045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ddccd94bee167ce63ec1f89cf94d8558fcd60a19d305e34b76a265e94cbea8e4`

```dockerfile
```

-	Layers:
	-	`sha256:aea0f5fa9a6bfb7d47e013190dbe91ecda564deb79f5390591ba599ce35cc1c2`  
		Last Modified: Wed, 17 Jun 2026 22:44:39 GMT  
		Size: 472.8 KB (472756 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de8e933fbf4d14f3b892456da5239468a0b23a674d11f5a7083df5f15ac77a54`  
		Last Modified: Wed, 17 Jun 2026 22:44:39 GMT  
		Size: 30.3 KB (30289 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:20a9e68b1f59c17c39790dd8b9bb189a5aa865886c813120523d50523a2d0dae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7554849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45ce8c3742ddc5ca55e8a7e9600a0879b5a9f2bba5840d933ac8adf6c67017b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 22:30:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:30:33 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:30:33 GMT
ENV PKG_RELEASE=1
# Wed, 17 Jun 2026 22:30:33 GMT
ENV DYNPKG_RELEASE=1
# Wed, 17 Jun 2026 22:30:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:30:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:30:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:30:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:30:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:30:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:30:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:30:33 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:30:33 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:30:33 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65928c293aa284183adc2c51899157b94e01de8c4442fe7431b10bea9ddcda9`  
		Last Modified: Wed, 17 Jun 2026 22:30:38 GMT  
		Size: 4.0 MB (3978380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7dce995a857a39a62155046ef7d3a55414d08b550a7450b9851627edbdbdb1`  
		Last Modified: Wed, 17 Jun 2026 22:30:37 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3d3dd880a2a6a71f3920ae4fae998766a1e4c0d3de7d25993c5eea7a3f4c99`  
		Last Modified: Wed, 17 Jun 2026 22:30:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:132263701ff800896df59f2adcad0697c725beb75b84aaed76d947fbf20e64ba`  
		Last Modified: Wed, 17 Jun 2026 22:30:37 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b16471a20bd434850d867296b8ee5c1a4616084d42946f55b57834d2d13ea5e`  
		Last Modified: Wed, 17 Jun 2026 22:30:38 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b03aac113518d8998b773b54f4c3b21c99a0f9c6c5e421dbe31b13905c58ea57`  
		Last Modified: Wed, 17 Jun 2026 22:30:39 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:cde8949539989dd3ea03ec6868e0dd387c4dd61f1a7fbd205b71b67d1401eeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6139ffd5afd2d9907c68e3c6b45c253d449110994698dda0f5490dd95faf2d0`

```dockerfile
```

-	Layers:
	-	`sha256:5ed411781d2193955b03978112d4924248980f3874b3d3da637e0158dad750b0`  
		Last Modified: Wed, 17 Jun 2026 22:30:37 GMT  
		Size: 30.2 KB (30170 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:aa0003042cd331e590741f220197913c03e5c71f9d31552736b5e2f801ace8cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.9 MB (6929084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b11896f76e359834cfa230e916abb3d57b533b10214d077c19891e3a4c2eb6f6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 22:31:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:31:31 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:31:31 GMT
ENV PKG_RELEASE=1
# Wed, 17 Jun 2026 22:31:31 GMT
ENV DYNPKG_RELEASE=1
# Wed, 17 Jun 2026 22:31:31 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:31:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:31:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:31:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:31:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:31:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:31:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:31:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:31:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:31:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d234173a5a456d144065eaed1993337a6113d8f8e6e8d7f6d6dd191ac7551a4`  
		Last Modified: Wed, 17 Jun 2026 22:31:36 GMT  
		Size: 3.6 MB (3641367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bf34eb9941efa9b4bbdf3727de3d8381fce13184bb941fb900be93a4f1d5e32`  
		Last Modified: Wed, 17 Jun 2026 22:31:36 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67f0b979792e5db0a49839ee6d532ef05f650e604acd3a03471f8c8996f3f75b`  
		Last Modified: Wed, 17 Jun 2026 22:31:36 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5638c5bd87b97640b19417fd7a1da09813901c3a87ee0952d6c3c0fb6bd82e1c`  
		Last Modified: Wed, 17 Jun 2026 22:31:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:811e51fd177b2010e443f47d52b478a5751e867f20778cfbe758d43512935ae0`  
		Last Modified: Wed, 17 Jun 2026 22:31:37 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:451cf0d7d223762e09d3ad3b0b6706d13187a63f6f96a5bcc4b3c676fa72dee5`  
		Last Modified: Wed, 17 Jun 2026 22:31:37 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6e0f9f20d7f7671d92462bf6cf544b0961bd3acbe738515697ab4b57048e54d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502543 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e53088c7bf7f225c59c702fb51add37fceebaea6b96cf07c645ce83edb1fdec5`

```dockerfile
```

-	Layers:
	-	`sha256:6826f148f394ae85b6a704b244a136141e5598e7a5a017cd29bc9612c9fc8aa4`  
		Last Modified: Wed, 17 Jun 2026 22:31:36 GMT  
		Size: 472.2 KB (472158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e7ca819a4128b97850306e0fd9ebfdcdd9f3f0ca0ef6fe7a0cd8b7bdbf12fba`  
		Last Modified: Wed, 17 Jun 2026 22:31:36 GMT  
		Size: 30.4 KB (30385 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:f9a50821ab66f42982f6b5d5a24d8ab84a83a2065cea934248a8dfa220b1df9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8862448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da342a6dedfb6ebcf7cb7dc2696cca49cbae3e3b7a254f2d085732c8c96a4427`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 22:32:28 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:32:28 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:32:28 GMT
ENV PKG_RELEASE=1
# Wed, 17 Jun 2026 22:32:28 GMT
ENV DYNPKG_RELEASE=1
# Wed, 17 Jun 2026 22:32:28 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:28 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:32:28 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:28 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:28 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:28 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:32:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:32:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:32:28 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06c03e7e1a50de31927db627b948f5ce73422b63e5cb576267e518c6eaa66b1e`  
		Last Modified: Wed, 17 Jun 2026 22:32:34 GMT  
		Size: 4.7 MB (4657987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d23151f25127e79cdf43d6581814a57bbe4335b7f95a7f2c4908a02854a76864`  
		Last Modified: Wed, 17 Jun 2026 22:32:34 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba7afaaac273517c60fa741edd8009ea4b9a1d71f4aa1b6ef856776d9836780c`  
		Last Modified: Wed, 17 Jun 2026 22:32:33 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecb093a46613e292a1717e226f77b5edf9407862350d5046cb0734d796d00996`  
		Last Modified: Wed, 17 Jun 2026 22:32:33 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d449f1c640fe854a8affcfe5f6c5c1aeb6d56f17495091c88a2ca59136b67577`  
		Last Modified: Wed, 17 Jun 2026 22:32:35 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20332a7c0b4c00bb43768785efddd867843e7ffe5a812743631fe834053ef118`  
		Last Modified: Wed, 17 Jun 2026 22:32:35 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:dd0575a6925b9ea2b68d1c203a9378784216966c56fc557171e483e208050041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.6 KB (502603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bccfdf6b5df1eafb332fc852b0b950ee4bac931c9fd3fe95a2c4d70b80b0484`

```dockerfile
```

-	Layers:
	-	`sha256:23ec3c38a9704ce6a8913332ab6edb6e4e4e1b1fa31a236c398407d47960205d`  
		Last Modified: Wed, 17 Jun 2026 22:32:33 GMT  
		Size: 472.2 KB (472186 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8735bed61a472ab687f636ff0d1e81d344f44cec18ae380dbfe66df527fa87db`  
		Last Modified: Wed, 17 Jun 2026 22:32:34 GMT  
		Size: 30.4 KB (30417 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:e0ce3a19af7fc65c15a237810147e411f20483b096d39486c9a2fc572329a9d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7917161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6825c6a493ca8cee770dd695be30d604d69e021410573bbf11f5491f4cb8c519`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 22:29:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:29:21 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:29:21 GMT
ENV PKG_RELEASE=1
# Wed, 17 Jun 2026 22:29:21 GMT
ENV DYNPKG_RELEASE=1
# Wed, 17 Jun 2026 22:29:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:29:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:29:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:29:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:29:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:29:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:29:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:29:21 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:29:21 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:29:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94c46333f1a0638104651476e5f33631fb5cc2e9c0f6b31ff0fca4316fbbc43`  
		Last Modified: Wed, 17 Jun 2026 22:29:26 GMT  
		Size: 4.2 MB (4222118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af152a4567d298f5ca61ca75eb1015fe4e4ed784910c9bdc1a4727111ad33f65`  
		Last Modified: Wed, 17 Jun 2026 22:29:26 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30787967d7ce8267aa6d263a769255b146a6c574eab00b101cba6907d99ca646`  
		Last Modified: Wed, 17 Jun 2026 22:29:26 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6311f8e4eb62c359b2fb7cfad0b14d3f40dee2b560ef1cad76dc0f1801c2f7ba`  
		Last Modified: Wed, 17 Jun 2026 22:29:26 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc86c97a0ec113178bf21cfb687fd75eeb42fc59da10c585aefba358e69b8c4`  
		Last Modified: Wed, 17 Jun 2026 22:29:27 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4310bf152f6a691f4d66eace257c808c80b78b36a0defca7c06f4a12b0d39243`  
		Last Modified: Wed, 17 Jun 2026 22:29:28 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:d8545dfc6ff9df8b641e82d1750991e2d858423e56cefda8cc17aecb51d105bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **503.0 KB (502968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:677a637c288b51f08b7fd8c4beb70132906248153b49bf5019c893d41ffe6f79`

```dockerfile
```

-	Layers:
	-	`sha256:3719f3ab9abd14f39b2c36d7007d6ea23cca87a5a083a21cedef2981d0e26834`  
		Last Modified: Wed, 17 Jun 2026 22:29:26 GMT  
		Size: 472.7 KB (472721 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6443265d5509d219fe29f27003a1bee6e545b945230cede5063b8b4e027a4890`  
		Last Modified: Wed, 17 Jun 2026 22:29:26 GMT  
		Size: 30.2 KB (30247 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:a6de20c8a0234041d79c164f3ebac5f98fed0d98bcb424dd53cc4e1c743947eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.1 MB (8138938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc6bcf8211a4e5279dc8537a0632402176e83a1a233e139bef4dc66bbe10ca7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 23:39:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 23:39:26 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 23:39:26 GMT
ENV PKG_RELEASE=1
# Wed, 17 Jun 2026 23:39:26 GMT
ENV DYNPKG_RELEASE=1
# Wed, 17 Jun 2026 23:39:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:39:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 23:39:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:39:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:39:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:39:27 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:39:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 23:39:27 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 23:39:27 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 23:39:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc05150e9a51fea0717c2b2f55ce33e58194e1c2bacc6add807a8001b9d05323`  
		Last Modified: Wed, 17 Jun 2026 23:39:38 GMT  
		Size: 4.3 MB (4303402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f9bf058e1b6afae091ef615e83767b636a0599b6b42a3a19335bf28110f3b4`  
		Last Modified: Wed, 17 Jun 2026 23:39:38 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99a5fc1280fa4a39653a3adb71b42da0bb3459378ca2e4401d63e2a4e97e1d5d`  
		Last Modified: Wed, 17 Jun 2026 23:39:38 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:513c7bcc18f89ca3a4ef627017a3301f662a9d9db5e884bbbdc44f02127ed258`  
		Last Modified: Wed, 17 Jun 2026 23:39:38 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2b13bca2119c0c13af3ca2d3c2b92bcb6dd4b924c7f2fb5dd62eab3866cc492`  
		Last Modified: Wed, 17 Jun 2026 23:39:39 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70356bfc4611531774601ea99c9ffa3192fe35bee90073219c2e534cab100a1b`  
		Last Modified: Wed, 17 Jun 2026 23:39:39 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:d2a0e36e02c674438192a67a485cb85d5051994aa2ebcb59aa0ba82d079e72f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04cc1d90b6b657b1f62379a118a25ee870c2d096fca54a552ea6b961d1e4f5a`

```dockerfile
```

-	Layers:
	-	`sha256:96c8c0100524eff645e196afeb2205635f638e9c79438858c962560c58d0dc78`  
		Last Modified: Wed, 17 Jun 2026 23:39:38 GMT  
		Size: 472.2 KB (472151 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3343c8c466d29440f94e82f720ae903933e11a6c9688edb539ebad273b66c7f7`  
		Last Modified: Wed, 17 Jun 2026 23:39:38 GMT  
		Size: 30.3 KB (30344 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:50f994d8456589b00c6ca26c1c08ea11fcc58f2104f1989ac8f4c8657f4a48d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7643889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca04883b08567670d97cb4520c412c0bfc38944f34c0491d58b9d79852f9820`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Fri, 19 Jun 2026 18:50:11 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 19 Jun 2026 18:50:11 GMT
ENV NGINX_VERSION=1.30.3
# Fri, 19 Jun 2026 18:50:11 GMT
ENV PKG_RELEASE=1
# Fri, 19 Jun 2026 18:50:11 GMT
ENV DYNPKG_RELEASE=1
# Fri, 19 Jun 2026 18:50:11 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 19 Jun 2026 18:50:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 19 Jun 2026 18:50:12 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 19 Jun 2026 18:50:12 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 19 Jun 2026 18:50:12 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 19 Jun 2026 18:50:12 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 19 Jun 2026 18:50:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 19 Jun 2026 18:50:12 GMT
EXPOSE map[80/tcp:{}]
# Fri, 19 Jun 2026 18:50:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 19 Jun 2026 18:50:12 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0ffec6d33b5cb3f9ccc256cd623eecd1679b33518ab83934d22b65f6038ee3`  
		Last Modified: Fri, 19 Jun 2026 18:50:40 GMT  
		Size: 4.1 MB (4051622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af1a6d01a046bc3c1b2289708ab6fb6e4716459917ffde4ceab0718bdec4487d`  
		Last Modified: Fri, 19 Jun 2026 18:50:39 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ae021284d8ad78d0f64e707226be257f8c922ad352329e00a07d048bae5a88`  
		Last Modified: Fri, 19 Jun 2026 18:50:40 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d98bd6ef29a9884cb688acaab392723452c343d47d4ffead0079493e72b93f6`  
		Last Modified: Fri, 19 Jun 2026 18:50:40 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2d7db392cd368faa2c520ad95a30921eb2563c65f0b8f22ad4282cfc9b629d2`  
		Last Modified: Fri, 19 Jun 2026 18:50:41 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59b9bd5625841791ba6b0e8b75840794367f1b2a657b9c0cc5dda44a5324ecb8`  
		Last Modified: Fri, 19 Jun 2026 18:50:41 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:10d354e64256cf43fb37fbf912f620a9b056c9d5ba29880d600180918bd2d3e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5be0f7bb2b78ae38a973f78e6bc7c1147c7189f665243539268b6f3031e036f`

```dockerfile
```

-	Layers:
	-	`sha256:08197568f4ced0cb6ffda1246e71620c9f7fb8fd23da93b1832e15a1be635835`  
		Last Modified: Fri, 19 Jun 2026 18:50:40 GMT  
		Size: 472.1 KB (472147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b36227205b7f1bfd66c587490ab3bcbd336bf91cb3063e9821de581378e7413f`  
		Last Modified: Fri, 19 Jun 2026 18:50:40 GMT  
		Size: 30.3 KB (30345 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:77b8f083deeed757f81aade2f59c070d2a78e4e8ffc1f79fd3b508f860bc2338
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7962374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18d35f66d7250e8af0d117b2b1a5ce5b9bf9eeeb5dda9dc9a8c6f68caa048cb1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 17 Jun 2026 23:02:27 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 23:02:27 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 23:02:27 GMT
ENV PKG_RELEASE=1
# Wed, 17 Jun 2026 23:02:27 GMT
ENV DYNPKG_RELEASE=1
# Wed, 17 Jun 2026 23:02:27 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:02:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 23:02:28 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:02:28 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:02:28 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:02:28 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:02:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 23:02:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 23:02:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 23:02:28 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc8bb239de81d6fdff950093b59cd3087679a263346f2bebbee3c2bebd729332`  
		Last Modified: Wed, 17 Jun 2026 23:02:37 GMT  
		Size: 4.2 MB (4231241 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a771299ca7c15ce10058b223c32aa8ba6f723c52749846fef0b09076dd485e4`  
		Last Modified: Wed, 17 Jun 2026 23:02:37 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce93b0445c1ed7df8929e100bd695018a8199fbf410561e176f94041f7a14fa1`  
		Last Modified: Wed, 17 Jun 2026 23:02:37 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6de2d7c98c732c09f829576b7e64dc5c4869ad405d80446db887b5db45af27e1`  
		Last Modified: Wed, 17 Jun 2026 23:02:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15f35b5fcaec808ebcc4fb63a9f7de9a7a01692ddff3068b8d6c3933637aa3f5`  
		Last Modified: Wed, 17 Jun 2026 23:02:38 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7043c21868d0341018d31e6c9393ac0095b49bb5a7566d7ce61a7968decbaf20`  
		Last Modified: Wed, 17 Jun 2026 23:02:38 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:263beca67014016bd9aabb876386a4222ad1d42e4584baa86c8ef7a06e31ed1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd5567f67b04f32d6e6bbda10d55e859afe7497e8c17fdfeaac6a5b3d542175`

```dockerfile
```

-	Layers:
	-	`sha256:d2b859a90fadd7f2b05fd67df2802cf4a093dd80126d8c9d73dadb31df55d4a2`  
		Last Modified: Wed, 17 Jun 2026 23:02:37 GMT  
		Size: 472.1 KB (472105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:952923ff57ed551aae7f5c9c27752b6dbd2df27f0846615b4d092f471bf34524`  
		Last Modified: Wed, 17 Jun 2026 23:02:37 GMT  
		Size: 30.3 KB (30288 bytes)  
		MIME: application/vnd.in-toto+json
