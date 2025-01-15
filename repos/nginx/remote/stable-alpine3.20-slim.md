## `nginx:stable-alpine3.20-slim`

```console
$ docker pull nginx@sha256:1d541dc68a99c4da7923e88b8e184f85034804a1ff59ee838a81d83c319267d8
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

### `nginx:stable-alpine3.20-slim` - linux; amd64

```console
$ docker pull nginx@sha256:d01ca4f305653c90fc9be8b1454fa71fd72ba9a52767df0c8ee06f85406ea1e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5384459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008f853bbf53f7efd88203b79b07da4f34f72502fe6223b55adce66498d0f2c1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425c7b6b0584ba3e78facb9a52bce0b3032548a747ea24fce89e69418b8ec85b`  
		Last Modified: Wed, 08 Jan 2025 17:58:28 GMT  
		Size: 1.8 MB (1753614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3151b8c48344fd76c43495924168f4eb016182e84c9eee19fa9dc110494bd0`  
		Last Modified: Wed, 08 Jan 2025 17:58:28 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32c1c5ad47053478e4726ed49aead7d7b704c6167ebcc47bb80e888bf608cdda`  
		Last Modified: Tue, 14 Jan 2025 20:33:09 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acc3b7ea73b8273e7aac52aa7fc506005290c7d574598acc30dcf5961e7e2972`  
		Last Modified: Tue, 14 Jan 2025 20:33:09 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b527c1980d3409f5c5d61d9a339ef1a703f0f7a3dad3f9af5465a2d86c6060b4`  
		Last Modified: Tue, 14 Jan 2025 20:33:09 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea697fe9913f548e3f99eee90b9715e8f14e83d578ee875fc40f3960d0e6780d`  
		Last Modified: Wed, 08 Jan 2025 17:58:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:f5ed31866dae4018216e100d1d81b62460b4afa7396792c6b37eb2c73ad65f97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 KB (492556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a75dcb982e7afe80646972bfdb1bbb3de92b683db1e3f14e294fadd4598ee95`

```dockerfile
```

-	Layers:
	-	`sha256:aa94d2828ebd82625359bff67579dfd70b4bbb0d91a62696140168ad22587e6e`  
		Last Modified: Tue, 14 Jan 2025 21:30:02 GMT  
		Size: 463.1 KB (463086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cbe5b5e1dafacaa92e83e8d7955e7a88f6995732da267eef40739837dfe3a03`  
		Last Modified: Wed, 08 Jan 2025 17:58:28 GMT  
		Size: 29.5 KB (29470 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:d8ac38fbe1014228b01486dc55188031b16a905240dac9da42f2b3f8321f8438
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5271538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c024f63c05399ae90b791beba63d0a79d7f78d745cae832e6465ee855e00c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Wed, 08 Jan 2025 17:23:56 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44398de13cb5560898ed839a81e82e74e4020c557f00522c86972335fd814a2e`  
		Last Modified: Wed, 15 Jan 2025 03:05:26 GMT  
		Size: 1.9 MB (1895465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179c29e5b5124b5a1cc00d6584cd7e2472ce62de938c87d15df7d9d485a60913`  
		Last Modified: Tue, 07 Jan 2025 20:01:44 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0681f5f1e23b339aed2c3b9398c45dd05f50165a8596b1c0462b158211e05ee`  
		Last Modified: Wed, 08 Jan 2025 18:45:37 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d445e2554ceb9fb2b9631223f114e63ca9d2c5aadaeddce4167a47e796580e6`  
		Last Modified: Wed, 15 Jan 2025 04:25:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9d1f5353211c8526da937be4919e432f4f8927a052f6c669a8a1f876104d1e4`  
		Last Modified: Wed, 15 Jan 2025 08:07:07 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa3f16cfd5c85f7376ba975069a0ea21ca59fc73923b82e98c7b728ecfcd4ded`  
		Last Modified: Wed, 15 Jan 2025 01:01:06 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:279629f2a95be5c44a379820438ad4e2bb6bfec2ea169c6c7c4365ff1ec7d4e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 KB (29347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:275d882399ab9b3bbc8ef92d587886cfc00521bdc09f753274a4263c016d56e1`

```dockerfile
```

-	Layers:
	-	`sha256:d8587355b59066dc8693b36db8e189d391b53edf43dec2bd1c856cc647d5132b`  
		Last Modified: Wed, 08 Jan 2025 18:45:37 GMT  
		Size: 29.3 KB (29347 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b553e46f4b0c71ea1f549d5ea99ec437e1c45efaad4318ee10652dd1cc24eb35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4826408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc74c1a6e54bf1a42256660aa0484b15c21dab2152e6b1f2ef2bacda8432f0f9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6072c096f1422e55a0ad5fde1a0280d18cacef2ba2bf8de408486fedbc8a7e26`  
		Last Modified: Wed, 15 Jan 2025 03:23:21 GMT  
		Size: 1.7 MB (1726300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:629b17ffac5f5673caddae3f0c4f82de5e72aa49d8d16874f5e9cb19da94837e`  
		Last Modified: Wed, 15 Jan 2025 01:01:14 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48612da33ab049916fedc0b4bdc6d7c37e57ca1cec7d077d117713ab03181369`  
		Last Modified: Wed, 08 Jan 2025 18:47:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68106c89dbbb34c81b6c9cf19652fb0323d2bf4f2178e8d7de30e94906b72556`  
		Last Modified: Wed, 15 Jan 2025 01:01:14 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af97cff047e7c67e73ce73a7d6cfa867e825ae04b9133b34b161ec037c2248e0`  
		Last Modified: Wed, 08 Jan 2025 18:47:37 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ce018b8470f1b2ce3c4b148dc497cad9725ae824ae4bf0526c4b1bffa2860a`  
		Last Modified: Wed, 15 Jan 2025 02:49:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:433308c8cb92f196a5717d4dba5656660f294b34aead78d31d32b7e676659da8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 KB (492700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b404fbd9f38131d745e04bed3066c6c650595f14cc5c34599a66cb879f5c35`

```dockerfile
```

-	Layers:
	-	`sha256:d94222f90594674a55a5770b81ecc90aff8ae6e9992089e3522bd19ee4a5b46b`  
		Last Modified: Tue, 14 Jan 2025 21:30:05 GMT  
		Size: 463.1 KB (463138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af65f86ea6eb96c55a3e5aaa257ed62f104b6c148784fdf9567032bf16cb2381`  
		Last Modified: Wed, 08 Jan 2025 18:47:36 GMT  
		Size: 29.6 KB (29562 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:286d508c96c9640dc06b09f097407048d10a40e207f9e2ace048c130eb51f156
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5882090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59270d64c2905d4747af27fbe79493271d9720871ffd983f2f5bfc15f177d4e0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c755bb4ce800c7c16418ee10f85541e6126a6cea245bdfae504e8ada56610d40`  
		Last Modified: Wed, 08 Jan 2025 18:43:47 GMT  
		Size: 1.8 MB (1786736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a0cf59c90048cebab50136551ce123fc95133ae1a3b93385fae9cfccbf0f2df`  
		Last Modified: Wed, 08 Jan 2025 18:43:47 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b0fe1b9a7675e503d0522a1f885fb7768abab722832b717449959a97dfc340b`  
		Last Modified: Wed, 08 Jan 2025 18:43:47 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49953a22b8235e7fecc726e04780604684f6a80d68a0b85a8e23a261e8b3853a`  
		Last Modified: Tue, 14 Jan 2025 20:33:18 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0048b09c95cb930a7474400517327a004e6cf58d30c2ec38341a102df2a353f8`  
		Last Modified: Tue, 14 Jan 2025 20:33:19 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9f498067717f6cf44dec220fa58374c24aa19c4c7ffa7542a2ef77dbd105655`  
		Last Modified: Wed, 08 Jan 2025 18:43:48 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:668c2ff5b42f5536dcfbca00f3fbaf7710007a30e56d61a74a7ea94fb57b40ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.8 KB (492764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd6d5e4d2b9856517d6ee8c787b10d07fad0e0a82c2bc43a6205a8286eaa3160`

```dockerfile
```

-	Layers:
	-	`sha256:5ea96ae022ae2531857c97be32b6a4873c273358997233962114bfa8ff55dced`  
		Last Modified: Tue, 14 Jan 2025 21:30:07 GMT  
		Size: 463.2 KB (463166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f73c8aae78ca4112c7cfad1708848fcc909137594400a92d061f79f51cdb9a77`  
		Last Modified: Wed, 08 Jan 2025 18:43:47 GMT  
		Size: 29.6 KB (29598 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; 386

```console
$ docker pull nginx@sha256:74a374fc0e2153865d835b3f38f76ce39fca189073bf291f4b09e5b7c64f5d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5436037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6626d1db981720c6de70dc3d20fd559c1a5498bc108142efa239d9cd95dcfed7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Tue, 14 Jan 2025 21:25:38 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f59b86924e9bda57e1e1c671ff4640069048d6cc1c015111148cb2759ba394c`  
		Last Modified: Wed, 15 Jan 2025 00:03:26 GMT  
		Size: 2.0 MB (1960477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1c03a8b33398850861f7c647c1a048983b6ed76b7430d7d62f7845f81c53b1`  
		Last Modified: Wed, 08 Jan 2025 18:00:47 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83cea66766b891b3f977654a4e411ca3228960ad7655b29e1aa19887c390c9ee`  
		Last Modified: Wed, 08 Jan 2025 18:00:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfda846769463e1071a4dce37910248e63395868ba1ffa5e97f259c549c77444`  
		Last Modified: Wed, 15 Jan 2025 04:25:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0539b29030d25067d39e2ffbff044e798155f27af363b9651909be2a68b5cd3`  
		Last Modified: Wed, 15 Jan 2025 00:03:25 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05dbb6258a2644b406e9e2c9ee2c1d4b284be1159b23528d8642ba6415338e86`  
		Last Modified: Wed, 15 Jan 2025 00:03:26 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:55651adb5cad01939b4ff19c3400bcac81d1ec2e2fa0e9d136305c990f40433a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.5 KB (492479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f87451e759d727e0a758b3cafbc41ca0a72190b903b402578ad1fc75309046d`

```dockerfile
```

-	Layers:
	-	`sha256:b8b04d7c5e32e5da4e7ec3434779b27722902c2499e6667f2d1083024cc54dc4`  
		Last Modified: Wed, 08 Jan 2025 18:00:49 GMT  
		Size: 463.1 KB (463051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9118f872c1d9cd3baba8ca40c84f4a3dcbe9c1772def74166234328b767176c`  
		Last Modified: Tue, 14 Jan 2025 21:30:08 GMT  
		Size: 29.4 KB (29428 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:6696425c5225cb0470414c35e41d7038106311b0bd19b809ad4178ccc99ef36d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5529338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8433d3de0e3bb1723ef7c7962b3f4f624cf703394fba8c558a011873e5b3efa4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Tue, 14 Jan 2025 20:57:44 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4498b9daaaea598b3cf9b480949eaddd0f065c8c7552dd8ab17b55919a9377e0`  
		Last Modified: Wed, 08 Jan 2025 18:31:28 GMT  
		Size: 2.0 MB (1950353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70545b107ec5661ee69a1d82ae729ebbaac2b102567e2f335b29561260fbb0dd`  
		Last Modified: Wed, 08 Jan 2025 18:31:28 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f02fea5d6bd9064eb0f348afe3c08c35cee7dad18fc084eb231bf606a8e5b322`  
		Last Modified: Tue, 14 Jan 2025 20:57:43 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfbd772f64b400d59998a051b2edd19f07880a31cf9acb09118eeed6479bb6e9`  
		Last Modified: Tue, 14 Jan 2025 20:39:49 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2593e9a7061c2583a0a9429e3b4127b18b29191afe2e017192f6fd159dbdbaf7`  
		Last Modified: Tue, 14 Jan 2025 20:57:43 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6d96d0696fb98146218a4a6840a28ec9e2a2fb91c8a61b327dcf374cc8f1a46`  
		Last Modified: Wed, 08 Jan 2025 18:31:29 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:e263a628ec0fb9717bc6e4e088270b4b7557ef0f0d3ad921d497a2e733fdae23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 KB (490705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954dc53643a7cb38418219f3f88cd9a18e98fd7e0a5b15054bbca03b070b5dc4`

```dockerfile
```

-	Layers:
	-	`sha256:209d067da876d865fc70721aa71da32d7ea62d77a35aaf41bb2392b77bd09321`  
		Last Modified: Tue, 14 Jan 2025 21:30:10 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90e608ee784e94debbe0c8de49cad2b320edae6221ebb2bd6288e0518bc2024e`  
		Last Modified: Tue, 14 Jan 2025 21:30:11 GMT  
		Size: 29.5 KB (29524 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:3a4cf4da32a8a498d7919b5f2c264802f07bc550b77d1784c0dd68f31a5f0031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5309907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54aed419aafbc63c680a412c3f1d5aeff4c3a8dad888bfaa3035eca807360276`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea1e6c3ca6ff9a20cf4bd0c526e9657466434536492904dbfc6cda571c15d83`  
		Last Modified: Wed, 15 Jan 2025 03:05:33 GMT  
		Size: 1.9 MB (1933386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78f48739e4e91c79e40a028d3990e5c329d6d820f0b924f0acb89c719c06b8a1`  
		Last Modified: Wed, 15 Jan 2025 03:05:33 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1149cdfcffb6cd63b3601d59a4859b6b66884ecb5e5dd026829010ac8aa12e`  
		Last Modified: Wed, 08 Jan 2025 22:27:16 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d809a9c93d24dcdbbd167dcae88face80acbae42b701057ea9b77bcd2626daa3`  
		Last Modified: Wed, 15 Jan 2025 01:01:52 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb144c1b4bf919fea852ff6e8628565c0fc60502252c95f008cd7e3e545ac010`  
		Last Modified: Wed, 08 Jan 2025 22:27:17 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76cfbc1340ebeb7d59703cd84f2fa713386df7cff3d4dfb9d8e1f8aff3ec00d1`  
		Last Modified: Wed, 08 Jan 2025 22:27:17 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:25df26aefd960b04b297e1f474d6bebd7464b722d6c0e46b1b6e69afac560726
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 KB (490703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1b817ffd4878b1aa7f6ec5f522523af2b7d76f5341e556cf3c06eeaff4aa9e`

```dockerfile
```

-	Layers:
	-	`sha256:dda34500bf6b908e99e00f2b5ccc202fd269c030b40cf9b9cb4cc1ba4f73ce68`  
		Last Modified: Tue, 14 Jan 2025 21:30:37 GMT  
		Size: 461.2 KB (461177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48760c0d5e87863fba5c078e6c17d9deeb2c3d3a0300d041a02c2659f4526b5c`  
		Last Modified: Wed, 08 Jan 2025 22:27:17 GMT  
		Size: 29.5 KB (29526 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; s390x

```console
$ docker pull nginx@sha256:6834f842e62f02669bd0057e825ee9867ed8cde8dcd35d19c628606cb8ca4812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5449995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bcf7e9dd1ac519aad319d7bfc5792a08f7292e3b888bf4f992c72c421f04b022`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 15 Aug 2024 00:20:26 GMT
ENV NGINX_VERSION=1.26.2
# Thu, 15 Aug 2024 00:20:26 GMT
ENV PKG_RELEASE=1
# Thu, 15 Aug 2024 00:20:26 GMT
ENV DYNPKG_RELEASE=2
# Thu, 15 Aug 2024 00:20:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"825f610c44dfb97166112e6d060c0ba209a74f50e42c7c23a5b8742f468596f110bb1b4ca9299547a8a3d41f3a7caa864622f40f6c7bb4d8bab3d24880bdfb6a *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 15 Aug 2024 00:20:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 15 Aug 2024 00:20:26 GMT
EXPOSE map[80/tcp:{}]
# Thu, 15 Aug 2024 00:20:26 GMT
STOPSIGNAL SIGQUIT
# Thu, 15 Aug 2024 00:20:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e80304799a47194fb570a02f5240eb1746496749d56c621a1d4e1292183c798`  
		Last Modified: Wed, 08 Jan 2025 18:34:05 GMT  
		Size: 2.0 MB (1982084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b406038371a10c5854ad33a961328eaf92d4116b941a31976934ce22101be23`  
		Last Modified: Wed, 15 Jan 2025 00:00:25 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd7e1d9d9ddcbb1813d7f3b3923dbce0392e0858bd7ea787a6af464e6c7e01c`  
		Last Modified: Wed, 15 Jan 2025 00:00:28 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55090393a266619ec9516d8e8ba837d16ff24a09a115231c2226a82374844321`  
		Last Modified: Wed, 15 Jan 2025 01:02:03 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad260f7ae819204ef4805626c6a22bd8c982f6b884323e14f7d5d29651a2124`  
		Last Modified: Wed, 08 Jan 2025 18:34:06 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5886531bb403172c9d9d0d81a2dd19c2bb140e5b93072d7908ef883a5843a9c`  
		Last Modified: Wed, 15 Jan 2025 01:02:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:d5a319386aceea53c1abd64eca4d9ce37cf7f8b134a5ea5a35f67f0b756a714c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.6 KB (490605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba14936e8c2b228b9b7e14afdb7b58e97465293d707417ed8b42b33df777c819`

```dockerfile
```

-	Layers:
	-	`sha256:32e61772951ec45ed98dbd626c2f19fee8a95067b336d0576347d051253e48e3`  
		Last Modified: Tue, 14 Jan 2025 21:30:39 GMT  
		Size: 461.1 KB (461135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b23783ca9ed4ce758408b62f7de78fea8471a668913e9b57ae7ca00fbf850aa3`  
		Last Modified: Wed, 08 Jan 2025 18:34:05 GMT  
		Size: 29.5 KB (29470 bytes)  
		MIME: application/vnd.in-toto+json
