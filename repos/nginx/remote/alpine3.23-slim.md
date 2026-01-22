## `nginx:alpine3.23-slim`

```console
$ docker pull nginx@sha256:fc0cff8d49db19250104d2fba8bd1ee3fc2a09ed8163de582804e5d137df7821
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
$ docker pull nginx@sha256:a511307c71702f76015df555c9a6edd8742f6c08ef72f49eb30dce6fc6d4c616
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5720874 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1116c0b4246776619c123156a0497118aabf3cadf448634b8e546cfcec91c1cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:29 GMT
ADD alpine-minirootfs-3.23.2-x86_64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:29 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:41 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 18 Dec 2025 00:29:41 GMT
ENV NGINX_VERSION=1.29.4
# Thu, 18 Dec 2025 00:29:41 GMT
ENV PKG_RELEASE=1
# Thu, 18 Dec 2025 00:29:41 GMT
ENV DYNPKG_RELEASE=1
# Thu, 18 Dec 2025 00:29:41 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:41 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:29:41 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:41 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:41 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:41 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:29:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:29:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:29:41 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1074353eec0db2c1d81d5af2671e56e00cf5738486f5762609ea33d606f88612`  
		Last Modified: Wed, 17 Dec 2025 22:48:50 GMT  
		Size: 3.9 MB (3860104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f453064fd3e8a9754b6e51b86c637e13203cbfc748fcf73f3c8b2d10816ae3`  
		Last Modified: Thu, 18 Dec 2025 00:29:47 GMT  
		Size: 1.9 MB (1856182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567f84da6fbd4287d40a5837485469435c40a81f9a94e98395b6385d3600643a`  
		Last Modified: Thu, 18 Dec 2025 00:29:47 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da7c973d8b92a1555060972c8849a332c93bfe2608c11faeee2098c4cfbe8c3d`  
		Last Modified: Thu, 18 Dec 2025 00:29:57 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f95a0f3229b49e777082e801b882b13fcc5b4e389410ce8eb066f4d58c71b9`  
		Last Modified: Thu, 18 Dec 2025 00:29:47 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:085c5e5aaa8eb4b957ecf253c74f16a6a5551231de3fb7c3ac74814a6bf17e06`  
		Last Modified: Thu, 18 Dec 2025 00:29:48 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0abf9e5672665202e79f26f23ef5dbd12558e2ea51ac32807922ab76fdb24ab0`  
		Last Modified: Thu, 18 Dec 2025 00:30:00 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:a1ea16bad16b2bbac2d3fc812935163de95e032cb7562bad9c41e5c39040828a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 KB (502851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39277a37d3ea69684c1fa8f7c39d82cee7bd103394f8cf754f80b3f72dcd76fa`

```dockerfile
```

-	Layers:
	-	`sha256:d4d098ca792ab823569d91e7b0ff09f6f4e1118ac644fadbf94d8a5939c4b87f`  
		Last Modified: Thu, 18 Dec 2025 03:51:31 GMT  
		Size: 474.0 KB (473984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9df852dd49066717dda1c7d21c65300bb39b965914245a7d5370b57899ac2fba`  
		Last Modified: Thu, 18 Dec 2025 00:29:47 GMT  
		Size: 28.9 KB (28867 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:d17fda22f5fa6bc70fbcf3003fc5207af77c63108206a96339a9ab80f27ccbb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5427028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06343a0dbf19a9928a0f1e72a46cde871b95b09e5cb04bcbf2013221016fa891`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:14 GMT
ADD alpine-minirootfs-3.23.2-armhf.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:14 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 18 Dec 2025 00:28:31 GMT
ENV NGINX_VERSION=1.29.4
# Thu, 18 Dec 2025 00:28:31 GMT
ENV PKG_RELEASE=1
# Thu, 18 Dec 2025 00:28:31 GMT
ENV DYNPKG_RELEASE=1
# Thu, 18 Dec 2025 00:28:31 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:28:32 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:32 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:32 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:32 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:32 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:28:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:28:32 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:cd0fa7d4c99310a30bac99a15cc62d2f7c0326577b630f591cebdbe4ad202657`  
		Last Modified: Thu, 18 Dec 2025 00:12:19 GMT  
		Size: 3.6 MB (3568432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:283ac494be3968c92adcf0934067db073829fafbf5370e70a8144043b64d62bf`  
		Last Modified: Thu, 18 Dec 2025 00:28:37 GMT  
		Size: 1.9 MB (1853997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:814f092f31440d9b6ece25d6fb4344f11caeed0161301a6d342ad74176e92530`  
		Last Modified: Thu, 18 Dec 2025 00:28:36 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce9452565441be470f82d05ec70ebf8028d988df17de85f639f607fb0cf07335`  
		Last Modified: Thu, 18 Dec 2025 00:28:36 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9994bbf3af7acedda000513e86f58932b5d69e79aaad050740c8cfd9eac2d607`  
		Last Modified: Thu, 18 Dec 2025 00:28:43 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:332d783258e756c7e9c61eb09c4fac49822ddd949d640ddc397f2a237500c28b`  
		Last Modified: Thu, 18 Dec 2025 00:28:43 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75d9c74a953e6f737e71b5741b27a9e978febd81074f9dc4ed6a9b8ab0db34ba`  
		Last Modified: Thu, 18 Dec 2025 00:28:37 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:f44de24e24c60db84165d7e8f5f0695154bd2972c2bbeff8c4575ef1bd00e02f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 KB (28779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:499258ce96e6dffd3eecbc42c4152ea00f1d393329c78f8c79b144026885d03a`

```dockerfile
```

-	Layers:
	-	`sha256:e5b6973e1c4c12cb04eb9413308327bcd50f59de98bd02eb1364204347f51187`  
		Last Modified: Thu, 18 Dec 2025 00:28:36 GMT  
		Size: 28.8 KB (28779 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:7edadf0de0564cc344e6dff6a065cc82b87f04134cb326799819b6c49ecc89f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4967121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b003f2b8db88d93ee4672780fdbd1a7faf1360e100a269f03bbf1e349e68ddbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:23 GMT
ADD alpine-minirootfs-3.23.2-armv7.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:23 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:28:00 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 18 Dec 2025 00:28:00 GMT
ENV NGINX_VERSION=1.29.4
# Thu, 18 Dec 2025 00:28:00 GMT
ENV PKG_RELEASE=1
# Thu, 18 Dec 2025 00:28:00 GMT
ENV DYNPKG_RELEASE=1
# Thu, 18 Dec 2025 00:28:00 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:28:00 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:00 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:00 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:00 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:28:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:28:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:28:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:28:00 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:fb78f26011a0b45e0ee3135541eee4683a4b98bf30b3d23f0981be37e8794a2a`  
		Last Modified: Thu, 18 Dec 2025 00:12:43 GMT  
		Size: 3.3 MB (3279388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d314d9421c11d2f36d10e0a15e53b408d18ccbf3709256d13fce3e67999406`  
		Last Modified: Thu, 18 Dec 2025 00:28:06 GMT  
		Size: 1.7 MB (1683136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:374098a089c102737e1acbc3300754ee6d2c35865915bb8ad9bae60a5671b0bc`  
		Last Modified: Thu, 18 Dec 2025 00:28:06 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a87906cb70726d993e49a654c112aab788436c8890f71b92093daeb641b9783`  
		Last Modified: Thu, 18 Dec 2025 00:28:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d7f2724432e363ddf6938a22eeaee0059b49749844d7f96ba3ed57dbb5ad107`  
		Last Modified: Thu, 18 Dec 2025 00:28:06 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d349003f71a0469081b06b19b90d292a5fae0b662729f950a72b37f77ef9d7c6`  
		Last Modified: Thu, 18 Dec 2025 00:28:07 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c84f335eb87049536b0c199c7596693c3670f47bb5bc81c11a9b8c5eae71561`  
		Last Modified: Thu, 18 Dec 2025 00:28:07 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:1dc35e1047c53e05b6b90fc3706b0bd6a42ae7a3e0e41f9ab137aa85ae49dfdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d6769352ecd4eacf9f28a0bdb9d8cc55364d702d1a194d853135905f098c5d6`

```dockerfile
```

-	Layers:
	-	`sha256:f634d788cf4946cd5039020f8a26ba2e0c865d5119940fa9cc6ff7389f60df3a`  
		Last Modified: Thu, 18 Dec 2025 03:51:46 GMT  
		Size: 473.4 KB (473418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e48171c567150b43349690a1d945434fff688a14b2f27f9c9d3a960181b56ab`  
		Last Modified: Thu, 18 Dec 2025 03:51:47 GMT  
		Size: 29.0 KB (28995 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:2a33b370329d21af89128caea1c493106b484380e27ab1f6122d71b7ac699b0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6073318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8bb700c36870e031205aa2a4ac25fbd6f0313692f44d4f7e11599939a821413`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 18 Dec 2025 00:12:28 GMT
ADD alpine-minirootfs-3.23.2-aarch64.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:12:28 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:29:32 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 18 Dec 2025 00:29:32 GMT
ENV NGINX_VERSION=1.29.4
# Thu, 18 Dec 2025 00:29:32 GMT
ENV PKG_RELEASE=1
# Thu, 18 Dec 2025 00:29:32 GMT
ENV DYNPKG_RELEASE=1
# Thu, 18 Dec 2025 00:29:32 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:32 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:29:32 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:32 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:32 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:32 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:29:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:29:32 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:29:32 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:29:32 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f6b4fb9446345fcad2db26eac181fef6c0a919c8a4fcccd3bea5deb7f6dff67e`  
		Last Modified: Thu, 18 Dec 2025 00:12:50 GMT  
		Size: 4.2 MB (4195739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0ef6d8231d0e512c7a0c0f7029bcfb8c77f0848b9cb8ec5373b28991c83415b`  
		Last Modified: Thu, 18 Dec 2025 00:29:38 GMT  
		Size: 1.9 MB (1872990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9076aaa4fd77085ce5562e9aca2b51ca88baf3fb8e41f8c777d0df14a1ce1085`  
		Last Modified: Thu, 18 Dec 2025 00:29:38 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0de4eea5b769c1703c4428a21cf0cce5b0a1668738391f1443979bb32cc9bc1`  
		Last Modified: Thu, 18 Dec 2025 00:29:37 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6628835d87d286d4d03f10b2c7f51d00f4556c49b5874947ce02609379069575`  
		Last Modified: Thu, 18 Dec 2025 00:29:44 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceb87b8ac279a84fc99bdc30e7406cf21bf5d5841819fd0e3c8e0c06d867533c`  
		Last Modified: Thu, 18 Dec 2025 00:29:44 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f04eae8d5eb8a0220a0d542da10f9c55b57a585dea1875cfbb1ee99d4c5a4a`  
		Last Modified: Thu, 18 Dec 2025 00:29:39 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8b539b6a8383c71b40e31dde6794bc086d6406098c5732f0b2c4251becc89d98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba7a510aef26fa7f3bb3db8e0488a630a5837b8a051ff6c15607311c34e43ad3`

```dockerfile
```

-	Layers:
	-	`sha256:f00453334a1d80d4f372c52a41c74bfbb44fc0b3e35a9048cbe612f4140377a2`  
		Last Modified: Thu, 18 Dec 2025 00:29:37 GMT  
		Size: 473.5 KB (473462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc56ec821a32bb63adab2492ee1bdd0fee609710c475b236162ac752eef760bf`  
		Last Modified: Thu, 18 Dec 2025 03:51:51 GMT  
		Size: 29.0 KB (29041 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; 386

```console
$ docker pull nginx@sha256:26b3457822a3906a3f38b6f7e82a03589d16f1c95e739c3242240905dabd7249
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5620345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf111b05fa79e5443dfe72f1e413718a903f565edeadb706c9ac1e2046a658a9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 18 Dec 2025 00:13:19 GMT
ADD alpine-minirootfs-3.23.2-x86.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:13:19 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 18 Dec 2025 00:30:56 GMT
ENV NGINX_VERSION=1.29.4
# Thu, 18 Dec 2025 00:30:56 GMT
ENV PKG_RELEASE=1
# Thu, 18 Dec 2025 00:30:56 GMT
ENV DYNPKG_RELEASE=1
# Thu, 18 Dec 2025 00:30:56 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:30:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:30:56 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:30:56 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:30:56 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:30:56 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:30:56 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:30:56 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:30:56 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:30:56 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c21df6a7383dfce37a4bfe31b291881f55907c419caf5d06cb6d699d290d0718`  
		Last Modified: Thu, 18 Dec 2025 00:13:25 GMT  
		Size: 3.7 MB (3686100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30f3b9423019844ed5f5c4f0297dfa0bd19221ef7a99123f1e9705ce865b8525`  
		Last Modified: Thu, 18 Dec 2025 00:31:02 GMT  
		Size: 1.9 MB (1929656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5479f44a40d942e7fde7691552e0602237ed857f048a0838d7531aa794a1d298`  
		Last Modified: Thu, 18 Dec 2025 00:31:08 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9406abd83b7d133a9ac3e4e0a90defc6cd0d597502dd6d068e0bb5b37f24c7`  
		Last Modified: Thu, 18 Dec 2025 00:31:09 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502579c506c585264f5a139e7698b0a70fb0b387fe962d071fecd3c274890927`  
		Last Modified: Thu, 18 Dec 2025 00:31:02 GMT  
		Size: 401.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700eb6e9438866a2fc45f6474447086813782c7f8be7d88907b5de3607dcc046`  
		Last Modified: Thu, 18 Dec 2025 00:31:03 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d474d44276717e74b2b65491ec42ca70b83b5473e8954d3f69ebda6a0e2c94d`  
		Last Modified: Thu, 18 Dec 2025 00:31:03 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:efc87ebe13500df8750bff63abab1ed5f944f33cc7b95f64be096d0917475cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.7 KB (502734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce8c7585504b826328375b536b31753ccd78d182cb92cba2150cae066a001775`

```dockerfile
```

-	Layers:
	-	`sha256:7801d3b592642dd6f4e98df153f883359315d1b80a77133f0581bdb18a8e7d15`  
		Last Modified: Thu, 18 Dec 2025 03:51:54 GMT  
		Size: 473.9 KB (473929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b37f1c11af7a183ee7c7d4627f10b4ce7e433c35092be6279fdf2b1974837b2`  
		Last Modified: Thu, 18 Dec 2025 03:51:55 GMT  
		Size: 28.8 KB (28805 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:9ea60e1e0cdcf52e88fc98b6b7f635d6c220d02aa181135a510bd528d68bd98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5779680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c6c05d58d92a302432f4c8710734d0236108ef4886640717e896027c12a62b3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:34 GMT
ADD alpine-minirootfs-3.23.2-ppc64le.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:34 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:35:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 18 Dec 2025 00:35:46 GMT
ENV NGINX_VERSION=1.29.4
# Thu, 18 Dec 2025 00:35:46 GMT
ENV PKG_RELEASE=1
# Thu, 18 Dec 2025 00:35:46 GMT
ENV DYNPKG_RELEASE=1
# Thu, 18 Dec 2025 00:35:46 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:35:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:35:48 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:35:50 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:35:50 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:35:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:35:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:35:51 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:35:51 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:35:51 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2dbbc2b20d556edcc853ddf744c4b2e946f16fba62ed0f0c4526533fdaa56e3b`  
		Last Modified: Thu, 18 Dec 2025 00:11:42 GMT  
		Size: 3.8 MB (3827755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7768ce352aefc992ae810af93735a85118ccdfec770872b483c4cc4b8e0060`  
		Last Modified: Thu, 18 Dec 2025 00:36:04 GMT  
		Size: 1.9 MB (1947329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79bcbc6920d77fa715571ed08e68ee0786a6f3acb9803eba1936d26c0f5a66ad`  
		Last Modified: Thu, 18 Dec 2025 00:36:12 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43085bafbfa8d79c1e78cbd5532b9c02c0afd51534a47ba03e559702dae4bef5`  
		Last Modified: Thu, 18 Dec 2025 00:36:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6e3a7e329e6401593dd4a2a3b9ed1e79913fa84fef504c363c5619d863338d1`  
		Last Modified: Thu, 18 Dec 2025 00:36:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f0bf37c16110480041f21fef3dd2b48950eb7f72223a4625c11602b075fca27`  
		Last Modified: Thu, 18 Dec 2025 00:36:05 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8969fd7f4b0740022a255737dfe18757174e4383f003e9af62cdbb88d765de2`  
		Last Modified: Thu, 18 Dec 2025 00:36:05 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:a733d8147be3bdcf48459dfb3586c3f9ff3170fb65f42698fd1a0602625b7fcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.3 KB (502349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7330a69d28a6ee08c7a919d5495a516edddb7455093aa97fe13402f8dbc26ca`

```dockerfile
```

-	Layers:
	-	`sha256:a4fca3f9ed57e4a9fcbc11e9993ba3804f73ed8ac02196c5ca2c956a8ce436f8`  
		Last Modified: Thu, 18 Dec 2025 03:51:58 GMT  
		Size: 473.4 KB (473403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:482ab49f430d0343f4b452409f3118554d77d5a8b54bb0677dd2e840a648cf4d`  
		Last Modified: Thu, 18 Dec 2025 03:51:59 GMT  
		Size: 28.9 KB (28946 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:6855787465997070524c5604e5a0f9788fcad8bd1703959cdc212d1a1c823bc8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5487377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39db4b5ec0ef9898235aa6fb86f0edb67a1892e32d4b3ab4a9de5068fa0d01d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 18 Dec 2025 02:40:00 GMT
ADD alpine-minirootfs-3.23.2-riscv64.tar.gz / # buildkit
# Thu, 18 Dec 2025 02:40:00 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 07:06:59 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 18 Dec 2025 07:06:59 GMT
ENV NGINX_VERSION=1.29.4
# Thu, 18 Dec 2025 07:06:59 GMT
ENV PKG_RELEASE=1
# Thu, 18 Dec 2025 07:06:59 GMT
ENV DYNPKG_RELEASE=1
# Thu, 18 Dec 2025 07:06:59 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 07:07:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 07:07:00 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 07:07:00 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 07:07:00 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 07:07:00 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 07:07:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 07:07:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 07:07:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 07:07:00 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b4b94acc94b4406ae94f444e29a6c06ae16918e74a98367370cf7529ea8d988c`  
		Last Modified: Thu, 18 Dec 2025 02:40:23 GMT  
		Size: 3.6 MB (3583938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b16df1ca313bb8ad780879742437c541a09a4712ae2354c45afbd8a40573ff2b`  
		Last Modified: Thu, 18 Dec 2025 07:07:32 GMT  
		Size: 1.9 MB (1898836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22cfda220ffaefe8d16c5dd1c23f4220af08793b52c487dc64853db9dd26e07`  
		Last Modified: Thu, 18 Dec 2025 07:07:25 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbbfa82ab1c368cbd4622aa298e65dbdeb3d41e48f61c628f4463a3c5ada1833`  
		Last Modified: Thu, 18 Dec 2025 07:07:32 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2c9037e58c1e5dadb260ffa210c8307ec753b27773ea60d84d76c9fc0438c1`  
		Last Modified: Thu, 18 Dec 2025 07:07:25 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbc714983e73721f1dabb872d583f0b1936e0654e3bf062287d5771593dfa458`  
		Last Modified: Thu, 18 Dec 2025 07:07:33 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4a2770cf3e76937b6e6f77ee30924dec6cb9235b4695e34dca1b57b2aa8c39`  
		Last Modified: Thu, 18 Dec 2025 07:07:32 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6e78a436ba6e23dd566ba8c00b5457b9ed49b9558a9cfcbfd189bbafec23e21e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.3 KB (502345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27fcdad13255dae31c110d4303835bc6da06a0679a8668dfa28d65fc0c6c923f`

```dockerfile
```

-	Layers:
	-	`sha256:f4e5901e1433ce5ec67a00c78e52cefbb2ea0667f14f0ab8f8629b1ab5e9997d`  
		Last Modified: Thu, 18 Dec 2025 09:50:35 GMT  
		Size: 473.4 KB (473399 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:caa023c84f1e011fba093837594e2b505650e5cd54afbe5b64ed3fe0071a5968`  
		Last Modified: Thu, 18 Dec 2025 07:07:25 GMT  
		Size: 28.9 KB (28946 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; s390x

```console
$ docker pull nginx@sha256:0416b3940411f887ecc78bf15d3040b57ac0941e2c322a9879105cf949468f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5701608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b0e32ad541cafd1d79b21492e9ddb3a523968076525e8798e8b08141d27279a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 18 Dec 2025 00:11:56 GMT
ADD alpine-minirootfs-3.23.2-s390x.tar.gz / # buildkit
# Thu, 18 Dec 2025 00:11:56 GMT
CMD ["/bin/sh"]
# Thu, 18 Dec 2025 00:31:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 18 Dec 2025 00:31:45 GMT
ENV NGINX_VERSION=1.29.4
# Thu, 18 Dec 2025 00:31:45 GMT
ENV PKG_RELEASE=1
# Thu, 18 Dec 2025 00:31:45 GMT
ENV DYNPKG_RELEASE=1
# Thu, 18 Dec 2025 00:31:45 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:31:46 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 18 Dec 2025 00:31:46 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:31:46 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:31:46 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:31:46 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 18 Dec 2025 00:31:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 18 Dec 2025 00:31:46 GMT
EXPOSE map[80/tcp:{}]
# Thu, 18 Dec 2025 00:31:46 GMT
STOPSIGNAL SIGQUIT
# Thu, 18 Dec 2025 00:31:46 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3d8fe54ac4e72ef775998241dc95a39f582dbddd5cf822b793130a331db6726f`  
		Last Modified: Thu, 18 Dec 2025 00:12:04 GMT  
		Size: 3.7 MB (3724311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eacc4533d62021954dd63740d2462a4d85f4fe61b81a3ce21a9872e4e094f0d`  
		Last Modified: Thu, 18 Dec 2025 00:32:08 GMT  
		Size: 2.0 MB (1972696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:660d3cbc27ec4f18d54c692cb6e5bd0522cec2dd0da5001a632c058df88add44`  
		Last Modified: Thu, 18 Dec 2025 00:32:01 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7474b1d59e8e77a28f0d896926cadccb585e1e37a78fbea77ed22da4999bca20`  
		Last Modified: Thu, 18 Dec 2025 00:32:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684c8f2232680b4a25b335a14493f855bbc6d2cf50ce0418cbb2e16abd430353`  
		Last Modified: Thu, 18 Dec 2025 00:32:01 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd2c6a76d2f83b60d6831241e6676b3e7a5c631f808d8165c15130684560d4b7`  
		Last Modified: Thu, 18 Dec 2025 00:32:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af93c89104079ae542dbc5753923a0b15bcd45a2b8331dccfc52002da5f3a6c8`  
		Last Modified: Thu, 18 Dec 2025 00:32:02 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:1463e703ea81de8e8706126dbe79977d8a625d9bd4b75066ac8699f23121d6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.2 KB (502200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7e9aab2bfae1bb87ef2a09a0645574be3f646e387e74c632a631efdf0406632`

```dockerfile
```

-	Layers:
	-	`sha256:e8f8a82a34fc7bed3787b3e6c07d76d2a95bd79c0ddbe33ee76142f7807f2a69`  
		Last Modified: Thu, 18 Dec 2025 03:52:04 GMT  
		Size: 473.3 KB (473333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d31e4427b3fb6bec5bfcb26b2c136bc175e383f30564014febf28660e07781c1`  
		Last Modified: Thu, 18 Dec 2025 03:52:05 GMT  
		Size: 28.9 KB (28867 bytes)  
		MIME: application/vnd.in-toto+json
