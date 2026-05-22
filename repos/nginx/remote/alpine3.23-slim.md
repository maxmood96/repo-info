## `nginx:alpine3.23-slim`

```console
$ docker pull nginx@sha256:803982d2a986185d428ab35e2226921e4c5cb254ef775498c8b3c2fbcb072b0a
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
$ docker pull nginx@sha256:74c5ea6b0fcd600958fe6ad3b97a58b6a04b28329121ac31ad8434bab87795c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5751669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c15775b5a7e1e3b403c660258be2d0cfa803db6f90250361457736f6b5640322`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:25:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:25:12 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:25:12 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:25:12 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:25:12 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && PKGOSSCHECKSUM=\"72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz\"                 && if [ \"\$(openssl sha512 -r b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && cd pkg-oss-b151aac903a6fc121d57f0909415381d0a1c1bbd                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:25:12 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:12 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:12 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:12 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:25:12 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:25:12 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:25:12 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abaae85d1626e429b3f1209aea369c0af9562cc06b5e075c006e0f699bba35f2`  
		Last Modified: Fri, 22 May 2026 18:25:18 GMT  
		Size: 1.9 MB (1882881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f834d60d8af3f133c7e76a202d28cd62cc026a561edca72ee752ef01bfaacd`  
		Last Modified: Fri, 22 May 2026 18:25:17 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de1b677d8c003ce9e558f3a0cd4dec3c035f424ecddd68063043a593ad572257`  
		Last Modified: Fri, 22 May 2026 18:25:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94d083cf706ab544ec7e9bcaba5c164db87b3d3a56176bf2fca440d535c16b0d`  
		Last Modified: Fri, 22 May 2026 18:25:17 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e654dbbbb9e15a1fa035d24728aeeb60bc655f4ebd4d6215a496b77a7d104697`  
		Last Modified: Fri, 22 May 2026 18:25:18 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5008f4a4b257356728e2feaf2b5b9e2054c0c577d324e76abbf14470b5f1cfd`  
		Last Modified: Fri, 22 May 2026 18:25:19 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:230fcde1ee45ff2a813d828999d0da5c9e07e714c2ffd957c35f2a5f98dc8434
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.7 KB (505710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c80784c97d902ae225e44a6b51d524f5e17132d58ec740cea5e0e57fcdd610e`

```dockerfile
```

-	Layers:
	-	`sha256:741a6b3fc8b6542e7a0ead452fbaa78c7d428c0244d9ba2de37193f203b01b1a`  
		Last Modified: Fri, 22 May 2026 18:25:17 GMT  
		Size: 474.0 KB (474012 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d180058feeda8e8e0403b243ccc2407acdce1fdec411bc06e39f5d3938d90aa1`  
		Last Modified: Fri, 22 May 2026 18:25:17 GMT  
		Size: 31.7 KB (31698 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:ec751e92c0eba0d7da1ce3c73596b895e4bbb3873ee730c9080d4c34ad0335a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460048 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87489bc39c5316f27a86bce3d9f223f742c36421f00bb8d05c7dd0afb3ea1d58`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:24:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:24:48 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:24:48 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:24:48 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:24:48 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && PKGOSSCHECKSUM=\"72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz\"                 && if [ \"\$(openssl sha512 -r b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && cd pkg-oss-b151aac903a6fc121d57f0909415381d0a1c1bbd                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:24:48 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:48 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:48 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:48 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:24:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:24:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:24:48 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c1202b7866ea5bf1c575559c804f619871b58042e94237caf39c1fd0f7e8364`  
		Last Modified: Fri, 22 May 2026 18:24:53 GMT  
		Size: 1.9 MB (1883587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b39c8651bd4eb65b3fa3363dedb0108baa6555b23431b4df76c1f4b5084b2aed`  
		Last Modified: Fri, 22 May 2026 18:24:33 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62b60924a0a7352ff7277c4585ce2ce7973f51dc88e4b9f30c8d7f7905b42cd0`  
		Last Modified: Fri, 22 May 2026 18:24:52 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1602275a212be2c5f2d20abba2de70da2f4a71860a06c330709ba32e33b36436`  
		Last Modified: Fri, 22 May 2026 18:24:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d96e1e8faeeaff02606c5c71479da4f60afba373053a38a4cbee4411f4dc48a3`  
		Last Modified: Fri, 22 May 2026 18:24:54 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50ee44c7df0ba2789fd917563805b87770e2233aa3c7dd44f7af20de68caa74c`  
		Last Modified: Fri, 22 May 2026 18:24:54 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:2ca35e118df109f6864146d3a7775808d276b97a7f9de54a2e3542b813b1defd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.6 KB (31609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0b64b1f687393fe4d86ed733544a17720f3fe90fcd09d0f906eff016be0a7b3`

```dockerfile
```

-	Layers:
	-	`sha256:95a4fac9563a2ff27aa7145e75d628b3cfef87a65181d84027125beb80318e2b`  
		Last Modified: Fri, 22 May 2026 18:24:53 GMT  
		Size: 31.6 KB (31609 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:868152878c9d5a4a74990146825faa9546d21b682df49b9e0fbfba96b7f38f19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4996316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:761fe5031f8167005e042672c7af2b265f3452365affdc4a8326cab0a8c9ef8e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:26:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:26:14 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:26:14 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:26:14 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:26:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && PKGOSSCHECKSUM=\"72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz\"                 && if [ \"\$(openssl sha512 -r b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && cd pkg-oss-b151aac903a6fc121d57f0909415381d0a1c1bbd                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:26:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:26:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:26:14 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:26:14 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:26:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7195e57e819bb6b3894121520b90c90290bf5d53071ee590c307fc50d46df01e`  
		Last Modified: Fri, 22 May 2026 18:26:19 GMT  
		Size: 1.7 MB (1708596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76130cbf7b50f812694552443c5304f4b93ff79b296704a9af6533f76ae3f588`  
		Last Modified: Fri, 22 May 2026 18:26:19 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8361a97cc63d7eb34b43b1eb75ad758f700e14ea3b54cb2234fcc048b942f6bb`  
		Last Modified: Fri, 22 May 2026 18:26:19 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30a1155e20d6b679e05233e180e533ba204e64533a3455c682c08d405f417500`  
		Last Modified: Fri, 22 May 2026 18:26:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b07a7fe1beba9c707384470df68d1a3a2ed81d44fe75e1c0f89c6d308697e67`  
		Last Modified: Fri, 22 May 2026 18:26:20 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:231eeb5c2f491bf763bdb395ef15cf402ece1efd420b06939b066cdfce9533b5`  
		Last Modified: Fri, 22 May 2026 18:26:20 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:0b3d9a602b6f9295914a6d265949764ce5c003ff4befdaa247b21f94e76e58e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.3 KB (505272 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c226062cb97b3610d0e1ee45ae8dc532517c72020a8bdd2ca450df9a4eadc5d7`

```dockerfile
```

-	Layers:
	-	`sha256:294098c94b469a25ef6dadc58011976f83e0e5d98b45d4f92c988f091671bc64`  
		Last Modified: Fri, 22 May 2026 18:26:19 GMT  
		Size: 473.4 KB (473446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9790f358977a4c80e00a0b39ddda91d236f5d7327079807ee72586f6005160c6`  
		Last Modified: Fri, 22 May 2026 18:26:19 GMT  
		Size: 31.8 KB (31826 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:f9cddce40dd0ee1f19ab533cf697894c88b013ef0cb472a010e2169c87e409b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6105922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca2a10399fc2f7c95d0b05a38076a6791b614b5c7f347166227b52e31a7649af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:25:47 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:25:47 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:25:47 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:25:47 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:25:47 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && PKGOSSCHECKSUM=\"72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz\"                 && if [ \"\$(openssl sha512 -r b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && cd pkg-oss-b151aac903a6fc121d57f0909415381d0a1c1bbd                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:25:47 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:47 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:47 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:47 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:25:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:25:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:25:47 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0a8eb1892ac4132988ce4aac8c4ff3599487a01129511f6fb60d01fae9a9351`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 1.9 MB (1901458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fd1853467817272c4f31287383a55bf275577631264f19faad90957276b29b`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dd0c1727b8e6406c345db087efe55647e6859013a66c6b5c86ed67210d9eef7`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58dfa199cc5789b16341ebe3ed56e76da7ff322bb3082e5dbdf9f4b2f12091ef`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79429faec0285d972d39bba343882b287ac08c1e7766951e257d4bcd838f42ed`  
		Last Modified: Fri, 22 May 2026 18:25:54 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92c8eaa0c5e2811db8e51fe7f7b46319d9262ceebd17b874a5b77f81e296d1fd`  
		Last Modified: Fri, 22 May 2026 18:25:54 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:15fed66ae63deb974d64d69fde9a30efaf57138388fe9b756481d58053a4abad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.4 KB (505364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21b97591a412dbaea3b744a0f95b089fb39936be462a7b5a0b041ed8607bed`

```dockerfile
```

-	Layers:
	-	`sha256:2912bf6312b6a8a765021831ca5dec782b6ccdd147007d5bb0e6bf7ad49aa10e`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 473.5 KB (473490 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bf24660ca53f26ee7a71611596da2e84cb32831d2cf421faf7de2f6f1c1e9f9`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 31.9 KB (31874 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; 386

```console
$ docker pull nginx@sha256:8b227fdcf39d42cc40b0094c4f7411dcbd393f62753d48e40981c7579ec94d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5650445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435090cd098705b4ee3b4db342b6d584a3bc8c78857df26e6c7590404b2e8578`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:25:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:25:48 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:25:48 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:25:48 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:25:48 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && PKGOSSCHECKSUM=\"72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz\"                 && if [ \"\$(openssl sha512 -r b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && cd pkg-oss-b151aac903a6fc121d57f0909415381d0a1c1bbd                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:25:48 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:48 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:48 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:48 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:25:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:25:48 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:25:48 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:25:48 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ba5e6133543bd01991e3c3dbc63177722ac3e3d82a69c34a1facc3b210b9d1`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 2.0 MB (1955402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88ff0ee296151cbcae4884badeb1b5c0e85347ce0e6cb2d48b73686daa762984`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327efd02d83aa42b49436285679d06d5b27ec2a9b6aeb38f122e6749a5da40db`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24191ed616075813b113df6fda60c35f62a7f8d9b7ac3acb1685e675086f0028`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d1eea1ed7bdf2e3758a4f264154a64683d39150440ac689c1404f1efb58a0c`  
		Last Modified: Fri, 22 May 2026 18:25:54 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27d10ead00a920fcc7f9e2b90a980643b615a2fae66a3a2c1235622c1a4b06db`  
		Last Modified: Fri, 22 May 2026 18:25:54 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:bb059ade0f32a494b740d47ca164fda958d65b2d58270105320436de4f48a926
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.6 KB (505593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:979b962a2f2cb46b29ef99c04956ac35fefa14c1e76abf9802566c4adebbe91f`

```dockerfile
```

-	Layers:
	-	`sha256:16ee7a4408dd439c933cf97d3624eb6204f4ee02aa6729ce9f682a776b331b25`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 474.0 KB (473957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10f89e294c68d0c4d9d664d55479c34b62df5bb949fa4fb47442b15fe83ec0f2`  
		Last Modified: Fri, 22 May 2026 18:25:53 GMT  
		Size: 31.6 KB (31636 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:7a0b11ec703b48d01f070f3b61733e0dc667ff7f865df0592abf39a0db7a97c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5810754 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b7f5944483932eb7c7df0c6addc73cc3190732994095b4a58ed594414090901`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:24:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:24:09 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:24:09 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:24:09 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:24:09 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && PKGOSSCHECKSUM=\"72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz\"                 && if [ \"\$(openssl sha512 -r b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && cd pkg-oss-b151aac903a6fc121d57f0909415381d0a1c1bbd                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:10 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:24:11 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:11 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:12 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:13 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:24:13 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:24:13 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:24:13 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93f40e4a067f032ceb87edac221b5edacf0b8a1d430e32bb1fa5eda5adb22f6`  
		Last Modified: Fri, 22 May 2026 18:24:26 GMT  
		Size: 2.0 MB (1975230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9502e284b60e9744732338927f9b165a87d3ba37612f60c1c0fc0bfd01b71ae6`  
		Last Modified: Fri, 22 May 2026 18:24:26 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:161087cc42b3d9b277f2df247effff0532ea1e02892e3b37fca8c73f3f47435f`  
		Last Modified: Fri, 22 May 2026 18:24:25 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3cf703fc1bb3484cb0dfdf28855ad40f0b941531db0fa5d6cc8c15a0d268593`  
		Last Modified: Fri, 22 May 2026 18:24:26 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3629e810c0333aab5d17376d88970295712e2a039e430ba7798b6fec15a9f2f`  
		Last Modified: Fri, 22 May 2026 18:24:27 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6cdd0ff1992631c05832ebe9200c6352cea03b43b7d50cfd8e8cb2b00067f653`  
		Last Modified: Fri, 22 May 2026 18:24:27 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:4a4917f584dbf49d90f37d59979e6c32cd0bbefe91b519c8646c3a7047729d5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.2 KB (505209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac75ef364aba431e64cd4fbd0e0f691691b71cbf2cef2997a0314982eeeab1fd`

```dockerfile
```

-	Layers:
	-	`sha256:3a4b4a2c2bd07d8442294ebd889e5a240eb72defaef2140fdabb2457f24c8bf9`  
		Last Modified: Fri, 22 May 2026 18:24:26 GMT  
		Size: 473.4 KB (473431 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f61d5faafc2e37581b34cb9d32e12cc4ea36654f80fe90cc25d27dc830e06c1`  
		Last Modified: Fri, 22 May 2026 18:24:25 GMT  
		Size: 31.8 KB (31778 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:492ecf9dbf235a6a2e516b48575eb49a426935dcd69b9881238013a10626ec9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5521511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:828da99e9c56651ccc0125c003874da39efa454a0f520f694494cc7e73699006`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 23:03:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 23:03:08 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 23:03:08 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 23:03:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 23:03:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && PKGOSSCHECKSUM=\"8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz\"                 && if [ \"\$(openssl sha512 -r 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 9d879d57ef75661eaed35e787ef434b2f85771f6.tar.gz                 && cd pkg-oss-9d879d57ef75661eaed35e787ef434b2f85771f6                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:03:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 23:03:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:03:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:03:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:03:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 23:03:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 23:03:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 23:03:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 23:03:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4cbb52e856db02714fa23fdb29b8719ebd51ef74fc2cea1e44ccbbf895aaf30`  
		Last Modified: Tue, 19 May 2026 23:03:33 GMT  
		Size: 1.9 MB (1929248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2cf2e1238006487832905a071b38e2585660aee305454de97390bd923c72158`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3da6b610e26f1fe7232d7a7c9fa6b5996f54af2dc50378cfbaafe99664583148`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9fd7ffb7d4781d6741aa98de2844fb77c559ad533fb2565fea2c7a4ae0f8942`  
		Last Modified: Tue, 19 May 2026 23:03:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4bdfa7826ed59b5a3fab101b3de18e4b53331cace8dff1b0163163d5f8c4e24`  
		Last Modified: Tue, 19 May 2026 23:03:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70b2a9e4747407cd1b2ed3e6012516c60967d1592a899e5ed3dcfa7227a9a9c1`  
		Last Modified: Tue, 19 May 2026 23:03:34 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b15a9f5bdb12df3ddd1616260cdc17169bf1b5206ecfca6542bd5bb06f2a4449
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.2 KB (505204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de5a7ad2eca161b01e4d2b69f82ed919a26b46c97171609e65cefad924f8e33b`

```dockerfile
```

-	Layers:
	-	`sha256:9635a3498775cef93398b303edd8e7913ffe2bf0d9fe3739c20e1732215e370d`  
		Last Modified: Tue, 19 May 2026 23:03:33 GMT  
		Size: 473.4 KB (473427 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3e334569c1226a9792cd11cbb6117a6a3ee8b7d990dc6bff77c1cb60dadff92c`  
		Last Modified: Tue, 19 May 2026 23:03:32 GMT  
		Size: 31.8 KB (31777 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; s390x

```console
$ docker pull nginx@sha256:bac7ca4c457c3ea5fdf6e6937c5f3d9ac52ab49574ccf5a2b2e3e33d812281a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5735226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc7dafef93d0d6c2cff9c62d380c31ab2e5bd3783c18a01bb63b5b82b7b3c9b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:27:59 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:27:59 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:27:59 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:27:59 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:27:59 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && PKGOSSCHECKSUM=\"72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz\"                 && if [ \"\$(openssl sha512 -r b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf b151aac903a6fc121d57f0909415381d0a1c1bbd.tar.gz                 && cd pkg-oss-b151aac903a6fc121d57f0909415381d0a1c1bbd                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:28:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:28:06 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:28:10 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:28:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:28:18 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:28:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:28:18 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:28:18 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:28:18 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44921dad87ba94a49ef3bdc51bb4b8225c82e2aafef2745851a910cdd3c2cbf`  
		Last Modified: Fri, 22 May 2026 18:29:51 GMT  
		Size: 2.0 MB (2004092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e28ae0759a528adf312b2873a4961eed55431a120cf1ebf26a8b38de53d3fe08`  
		Last Modified: Fri, 22 May 2026 18:29:51 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d76cc9e76ee2489216f15611aa22dde145067dddc328a0b2be5b05b845a4891`  
		Last Modified: Fri, 22 May 2026 18:29:51 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b3a5cc9aca0cb438e6f475f7d0e876e4de0f73cc0e72258f92af8cb17fc18e9`  
		Last Modified: Fri, 22 May 2026 18:29:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3be4f62e0bb67ad51d48a482b8c961541fc010067bb622f2b1f6377489ba64da`  
		Last Modified: Fri, 22 May 2026 18:29:52 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7163dcb6f888fb54a9516657c10eb242dc015a4c33d368297e5dbe6310098e6`  
		Last Modified: Fri, 22 May 2026 18:29:52 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:a7e92f06b22e4d921868b6669d6c4715714704eb4c282d10a2c9881fab5eae66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **505.1 KB (505059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:424910866fdd3ff5dce2f6b6b45f1d48f95be9d10b88959d2802c71f5e72210d`

```dockerfile
```

-	Layers:
	-	`sha256:85c10684a8261de458dbbae45ba572b99fa75a6344a6b757494ab8eff011b513`  
		Last Modified: Fri, 22 May 2026 18:29:51 GMT  
		Size: 473.4 KB (473361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72841a720039afb38e43b3b25fc1976873e6446a6630a1fe1448897fda60a2a9`  
		Last Modified: Fri, 22 May 2026 18:29:51 GMT  
		Size: 31.7 KB (31698 bytes)  
		MIME: application/vnd.in-toto+json
