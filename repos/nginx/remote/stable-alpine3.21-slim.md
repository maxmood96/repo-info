## `nginx:stable-alpine3.21-slim`

```console
$ docker pull nginx@sha256:39a9a15e0a81914a96fa9ffa980cdfe08e2e5e73ae3424f341ad1f470147c413
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
$ docker pull nginx@sha256:5e36bd7a8adfe291560a6849d3125438fbe244f29a567522099caceef32bce54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5438257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b3e72e4373533cb8e5756880e7d9a97163740ee60cb7d0bee15db50293fc143`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f18232174bc91741fdf3da96d85011092101a032a93a388b79e99e69c2d5c870`  
		Last Modified: Fri, 14 Feb 2025 14:36:50 GMT  
		Size: 3.6 MB (3642247 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde65f7af9d6bd24c25436572f04a4590e1d24cc3261e490b4dc04f8ddc95f55`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 1.8 MB (1791419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532a231453496d98bd24f9d17442565e55a30c355843a7106ca30d455828ab0c`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbdf43ac95df903e0e0aba895e4fde36b9994a02e21e6f9ee01a90b874330b2b`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c544760e65143e93084253d9559bde21e5b5ed47cec5db7ffce3cf52c6c1ea4d`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc2eb67bce91b1eacb09e48d14caba02f056ba09772b34f083b54b7b369cc8c`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f9a172b25c0bb4945785ec1043c39f16f4af6efc5f40b0000ef423c84c1a1d`  
		Last Modified: Thu, 08 May 2025 17:04:39 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:5b4a4171cfc76d1e0e072d399cdb33be5623578af83e63c7caf96a6587f4603f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 KB (498938 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfa2ae235ce0560f50fef60aedcb7e7d539361ecffba3db0626e313936ad4c3`

```dockerfile
```

-	Layers:
	-	`sha256:ddb8dd07d8400fc02c5dac60bcf99980605f987aade884214ece90337297fc28`  
		Last Modified: Wed, 23 Apr 2025 18:51:21 GMT  
		Size: 471.3 KB (471311 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1be37bef14a5a83168c51d01f2fc78b71705d6fa814c10897a65ed3a35476d0f`  
		Last Modified: Wed, 23 Apr 2025 18:51:20 GMT  
		Size: 27.6 KB (27627 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:328d4ef9d15fe532ad04159528642fd2096e4f3f7df4a123a974d2e8e2877c72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5157531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0aa14ca97eefd12ec32e7e658671e7a83ecb2aec093d314084afd16f1993747`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:76099982f06682e28a60c3b774ef20931d07b0a2f551203484e633d8c0361ee7`  
		Last Modified: Fri, 14 Feb 2025 19:24:56 GMT  
		Size: 3.4 MB (3364731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e16fd59453c10a1e295222fd4bd7a5ce7a34ea37f73afcd8c0c896053248d61d`  
		Last Modified: Thu, 08 May 2025 18:41:31 GMT  
		Size: 1.8 MB (1788212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69f4c676036f18e05826354a8d5b8eb1046400499bc277fbdd687548e2fac6b2`  
		Last Modified: Thu, 08 May 2025 18:41:30 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c9a258cd174638c4a39e5e1b1217e225182e8956e1264fb05a9a11f2586b298`  
		Last Modified: Thu, 08 May 2025 18:41:30 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3907a050d8ea026fa2c02376f2652e630943855c550037434fdf6bcfd55d5050`  
		Last Modified: Thu, 08 May 2025 18:41:30 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95b4f405938e0014608bad51726287a6b28ee30d41c6fcbd4e0f7161e874b426`  
		Last Modified: Thu, 08 May 2025 18:41:30 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b025e6ba6235153998f91a89ff9c4052a434e76bfdcc67a9f0078e880842376b`  
		Last Modified: Thu, 08 May 2025 18:41:30 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:0f341c786bf574ce89623a8d5f244eedb664def8a163ecf8a69b27249d39d2e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0fdedc55b4ef62aebddd7eb4edbc40760e84bef633346495779abb33d7b96f0`

```dockerfile
```

-	Layers:
	-	`sha256:29aadd3e1a949b87f7d9f2fb3c704612b07b3d137acba34bf83391868e8e7641`  
		Last Modified: Wed, 23 Apr 2025 18:51:40 GMT  
		Size: 27.5 KB (27504 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:372bda8ef88ef950f2e8581a599e57742fcf15b625a3f355e46ec82d87eb8021
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.7 MB (4725986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23f6c813a5204ca140ef65a78bfb02dffc568f8d7c7dec180815de848f3c5de`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:85f3b18f9f5a8655db86c6dfb02bb01011ffef63d10a173843c5c65c3e9137b7`  
		Last Modified: Fri, 14 Feb 2025 14:37:26 GMT  
		Size: 3.1 MB (3098123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e32b5b1eb77e54f3c588f4abb3a184c388ba8b11aec9124a167915e83ec29c70`  
		Last Modified: Thu, 08 May 2025 17:28:18 GMT  
		Size: 1.6 MB (1623268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a36207e437dbbcb0e48fed6055a9b51145c74df9e90310884d857c20065bcab`  
		Last Modified: Thu, 08 May 2025 17:28:15 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03d35cbc600a7c0c251be85ac408919dc8e7bcf78bbfbe82e2b412b8d535c982`  
		Last Modified: Thu, 08 May 2025 17:28:16 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03ca2d13aef1f199fefd9b87e1e371d2e4405e0054b90b3710217f1bc82e212b`  
		Last Modified: Thu, 08 May 2025 17:28:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86e9e1caa8195d5cbf6aace96e5205cd77a5cb51730a87559166d0c43d0f5510`  
		Last Modified: Thu, 08 May 2025 17:28:15 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4a57343389ed3fa43819c13a8b949c0e25e349e037784808fa75de7c0d84e2c`  
		Last Modified: Thu, 08 May 2025 17:28:15 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:afbec68c6327daaaa023acc00d80b1753c10f3d76164662270be0892c22eb12c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.1 KB (499082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84408169ce2363ff3923faade9bec1bb3487d3ae03dc2e0bf5550db6d6da8a98`

```dockerfile
```

-	Layers:
	-	`sha256:f66956adea7721b60c1d777189ad68a580d0b8130c0f8cd92c6e234bcecdd417`  
		Last Modified: Wed, 23 Apr 2025 18:57:30 GMT  
		Size: 471.4 KB (471363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ebd5ef3c081f1cc1e785be97fe3f99e6da1b93af8fe16eab575a125a0d46ae6`  
		Last Modified: Wed, 23 Apr 2025 18:57:29 GMT  
		Size: 27.7 KB (27719 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:d1ca6cd26599be6fbb447a2c7105e6b76c4d0eaf8b5c09d9841b8331a0e3ed3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5783468 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ea848ccd27824b1d9d3ba7bd534167ce751ab78508b1e12ba5b19308b5f4a67`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6e771e15690e2fabf2332d3a3b744495411d6e0b00b2aea64419b58b0066cf81`  
		Last Modified: Fri, 14 Feb 2025 14:37:30 GMT  
		Size: 4.0 MB (3993029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398035710bbd3270864d34b0d5c608aca864bbc0a4096fc451a0ddbac10a9ca9`  
		Last Modified: Thu, 08 May 2025 17:06:14 GMT  
		Size: 1.8 MB (1785850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af17ea29b1f576d9b1579c9e7224c405e9d48814f3eaee1fae1ccee388ad3c33`  
		Last Modified: Thu, 08 May 2025 17:06:13 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:529301633d0d8077f332b70350a341634520a7918323a3445872f6e22e0f5ddc`  
		Last Modified: Thu, 08 May 2025 17:06:13 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afdf9401d1b3d53bd417c4a1e54fb9505b8d7f8c7a329f3c2684c0d3bf2913c0`  
		Last Modified: Thu, 08 May 2025 17:06:13 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237618350fe059755be46df030e797fbd0fcddc00f176790a28d51d85fdcdeb6`  
		Last Modified: Thu, 08 May 2025 17:06:13 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b85fb7a148fb0423cebd671477471172a926e77f5e347dee68b3139bd2db852`  
		Last Modified: Thu, 08 May 2025 17:06:12 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6795ba748716208571463cf8fae1fd50811bccf9da8d7fb1a2b9cc4a4c8de45d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **499.1 KB (499146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6feee38f93ae29eb72b335de789ac2e01b2964c7b66da21f1a41f0d2cb0415b`

```dockerfile
```

-	Layers:
	-	`sha256:a3275f1c2f402add8d91d47d02cb16b9b32da3422c2ddbbba97182b4d5b8c513`  
		Last Modified: Wed, 23 Apr 2025 20:11:26 GMT  
		Size: 471.4 KB (471391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6baad2340959d1eb6ac540eb10c1c12c60be6e652693c1226452872f14b40ada`  
		Last Modified: Wed, 23 Apr 2025 20:11:26 GMT  
		Size: 27.8 KB (27755 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; 386

```console
$ docker pull nginx@sha256:d54ac0bb3e78d8c1ce3b2484523b09b69b500aa53561ab0dd8111a1fdfbcb99b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5329309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fda26cf6e615f70b26c40abdb06ae59c9fc9857187442f562a043b06faae1bd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:69aa61ccf55e5bf8e7a069b89e8afb42b4f3443b3785868795af8046d810d608`  
		Last Modified: Fri, 14 Feb 2025 14:38:41 GMT  
		Size: 3.5 MB (3463623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cde1a9f9bb7576a7c458d62ef84c39aa0ccd7f45ddc20f10e6715ef37163ccbf`  
		Last Modified: Thu, 08 May 2025 19:41:29 GMT  
		Size: 1.9 MB (1861087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d2ad742bd572bea8277a8e9f0c32d771acce297b57695e1e86aad12880f435`  
		Last Modified: Thu, 08 May 2025 17:10:39 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daeedb2b165e6f3a4856fb10a21a9b93c038ffaae47578147826a154dd368c24`  
		Last Modified: Thu, 08 May 2025 19:41:29 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4146e86aa9f2d5643b847c0b9064ded243d4ea3a3afe6a6f9f32d028bcdf7d1`  
		Last Modified: Thu, 08 May 2025 19:41:28 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:688f5119d74bb18be4542eeb2a9c0cb8c8dc62606a9f6762fa19fc865a3beecc`  
		Last Modified: Thu, 08 May 2025 19:41:28 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4580bb8f58269e3372debc5aa5ae859ba9adefde8b5ff6f78ab91f1b5bbd4e1f`  
		Last Modified: Thu, 08 May 2025 19:41:28 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:169648bbc83f576b052d0cf6cc3661288ef592b9947ced04d4e76da0281cd46e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **498.9 KB (498861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f34091373ed5185e2db1cd00be20d47f4a1c1cb1b711e1a33b143973de721f3`

```dockerfile
```

-	Layers:
	-	`sha256:2f9ee359e7906b8a4f4ebf33b5f50832f205f2e9fba4b4ed5e4fe6df3b87b475`  
		Last Modified: Wed, 23 Apr 2025 18:52:41 GMT  
		Size: 471.3 KB (471276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25398939cdf04ac6a47acfe42d70011c486d1fff88046a018ff15b5a49bb275b`  
		Last Modified: Wed, 23 Apr 2025 18:52:41 GMT  
		Size: 27.6 KB (27585 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:053b2bb170a0aed867a42c04670922db06d1b10c1e5d74b5a8ae1188f48c56bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5435723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef753173d28cb80d4f0684d637057f164ac28b8e994bfdd7d55b0e46d2da390`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:184b14480d317057da092a0994ad6baf4b2df588108f43969f8fd56f021af2c6`  
		Last Modified: Fri, 14 Feb 2025 14:38:03 GMT  
		Size: 3.6 MB (3574345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6310be32a6e2c463b519c022716c40559e0d0d9036a3286496be256bf87a7c46`  
		Last Modified: Wed, 23 Apr 2025 18:59:49 GMT  
		Size: 1.9 MB (1856781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d83e1b0f9281fd6a85fa98d942a4d13ec622c2c5247835c73b33d7008cb44b`  
		Last Modified: Wed, 23 Apr 2025 18:59:48 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea73dc48637addea66b341eaab3e6a6022907d1096b34ef142b1fbcb505e2f77`  
		Last Modified: Wed, 23 Apr 2025 18:59:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906f8695f21223da381d12826c611ea1a770e0d5abba3fa72d8431be9ede766c`  
		Last Modified: Wed, 23 Apr 2025 18:59:48 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6bc19a2ee1d06fd5773656fe793fc5548fc4127760e9d988a2f6a6647afb71b`  
		Last Modified: Wed, 23 Apr 2025 18:59:49 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ac1c260e96bb74cf489f9c207c7425292b3911724de10138a572dbc0c108962`  
		Last Modified: Wed, 23 Apr 2025 18:59:49 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c02922e2c1d694afbf390615f336dff55af038a6977d72d3b641d245f7846fcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.1 KB (497089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a7db793a40a8f24a6b3f0583166cf97673bcde456a0ba0aa831da631df025b6`

```dockerfile
```

-	Layers:
	-	`sha256:a3287bc72f6de55afb72420216759efc2c283cb429936650db4c48c1194b13d8`  
		Last Modified: Wed, 23 Apr 2025 18:59:49 GMT  
		Size: 469.4 KB (469406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d59f2c6ad20a7c22b6845c4eaab18ff188e530258997c05841f244073add657`  
		Last Modified: Wed, 23 Apr 2025 18:59:48 GMT  
		Size: 27.7 KB (27683 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:4dd96f442d896f13690dbaca2882204f59850d1727a0672850d60a17f2e39153
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5186323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:388810c340e2565decf08a2c9e64a53983daf80c96a65442812230826b628ff6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7df33f7ad8beb367ac09bdd1b2f220db3ee2bbdda14a6310d1340e5628b5ba88`  
		Last Modified: Fri, 14 Feb 2025 19:25:43 GMT  
		Size: 3.4 MB (3351439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa5fbdf5664a3d80b342c727cdb7c7912ba9c2111915c88f5304dbcaaebd6e10`  
		Last Modified: Wed, 23 Apr 2025 19:19:27 GMT  
		Size: 1.8 MB (1830282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6113465361ddbe2db756492ab6558f8fa5abd6e6737e0053ec522183c006af8b`  
		Last Modified: Wed, 23 Apr 2025 19:19:27 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75894e8c3f254fd32ca289b740b6876324dfd027b9d289c10d3dbfb3a3a957e5`  
		Last Modified: Wed, 23 Apr 2025 19:19:26 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:997a27bdf1f47c04a51c31ef848f2b4d401c22af86808383cafc03af7b754204`  
		Last Modified: Wed, 23 Apr 2025 19:19:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90182223a335eeb162d6b32615879248a0bd9892d1885b7984431ee3fe36c7ab`  
		Last Modified: Wed, 23 Apr 2025 19:19:28 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766265354a3c82af745f16559b2849a6eb729bd1c25b42fac67ae5b1ede9182d`  
		Last Modified: Wed, 23 Apr 2025 19:19:28 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:08705eadfaf141db4d326703b385f63f10b7559bd4b0503a56f9a737a2045677
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.1 KB (497085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34d6663853def72139256f65c1cd9f97bc2102222ae3973e900fb4a98675cccd`

```dockerfile
```

-	Layers:
	-	`sha256:3da31477627c65d1c36143e3db4e0409669378b9e7fe95dc972d9de3d85bd1d2`  
		Last Modified: Wed, 23 Apr 2025 19:19:27 GMT  
		Size: 469.4 KB (469402 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76cef109947c0c57efc6f9d7cf7f4b0f66fb0c105a80b137ef359f5535c73810`  
		Last Modified: Wed, 23 Apr 2025 19:19:27 GMT  
		Size: 27.7 KB (27683 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.21-slim` - linux; s390x

```console
$ docker pull nginx@sha256:cbfbbfd626e668934ea7173992499bec62de3d3d94717b62113c9e3289a8bd4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5364519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a0f77d41ceb340a1b53d38d3540e13e5e162304b7b41b027c9e20a53ba0d86`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:28:36 GMT
ADD alpine-minirootfs-3.21.3-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:28:36 GMT
CMD ["/bin/sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c1a599607158512214777614f916f8193d29fd34b656d47dfc26314af01e2af4`  
		Last Modified: Fri, 14 Feb 2025 14:38:37 GMT  
		Size: 3.5 MB (3467567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17773d7041e782bd949581f81e6bd82c5c7068193c6b8c9a4f55f5a5976bb84b`  
		Last Modified: Wed, 23 Apr 2025 18:56:33 GMT  
		Size: 1.9 MB (1892353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a032937d4c834f4e993837e80d74108f2bd1b43f615a274c874e0faa60ed3a74`  
		Last Modified: Wed, 23 Apr 2025 18:56:33 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7601719b11d14331a32f710f8f1628a3563ff16aabe4d490eab825e3730740f9`  
		Last Modified: Wed, 23 Apr 2025 18:56:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c1c8429dc9f97aecb0141e1b2ca60b57d0a238fc3ae6b13111a7b510260c79f`  
		Last Modified: Wed, 23 Apr 2025 18:56:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93271d8cad9ed68d60e24dc64e2a2910e305d2f6b9e8611f9da1e811511c7d0`  
		Last Modified: Wed, 23 Apr 2025 18:56:33 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b733ba68f83a6a7445d10713f17df2fac40eb96700092dc27f283b224aa2e8`  
		Last Modified: Wed, 23 Apr 2025 18:56:33 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.21-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:fdfee4f2f560c9eb07924fd6f8a56ec728ec7281df884fdd90f499f72f2231d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **497.0 KB (496987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af5a4ac0c893333f836b59863c7d618d1100a070b646f18731271f8367dbe33a`

```dockerfile
```

-	Layers:
	-	`sha256:f5f263a82780b2f4bf561b7bfc568bd1f409f59d76ee28076d4db78469c83379`  
		Last Modified: Wed, 23 Apr 2025 18:56:33 GMT  
		Size: 469.4 KB (469360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e07352f64b278ed756ff59b0816e5b2857931ba06e68c0613ffacacec18151b`  
		Last Modified: Wed, 23 Apr 2025 18:56:32 GMT  
		Size: 27.6 KB (27627 bytes)  
		MIME: application/vnd.in-toto+json
