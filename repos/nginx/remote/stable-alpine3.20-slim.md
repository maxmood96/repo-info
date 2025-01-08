## `nginx:stable-alpine3.20-slim`

```console
$ docker pull nginx@sha256:f996b474d3b41ca853a4b6335209e7f24d02568723668b81a60a4672c3dbb979
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
$ docker pull nginx@sha256:2a351905ca70d0c027e35904b9d358787c6124e470fed0054d90f3c16be006bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5372196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49981c5a4979994954b89480f6fade49ed03127e95c8b2a7fb17efb2293fb4f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
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
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa5b053edb3a73bdd0e8cb09a305d0a62e2f08782b52a2e8bb10c3983b8210d9`  
		Last Modified: Tue, 07 Jan 2025 03:20:26 GMT  
		Size: 1.8 MB (1753613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f48296187f491a5b5ebbe1bb43ce728267fafb6b35bfdb21021608b367cac5f`  
		Last Modified: Tue, 07 Jan 2025 03:20:26 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32bda9cf66a81b12941770aaee0fa3dedd0cb57ca037fd3cd2de68957e282063`  
		Last Modified: Tue, 07 Jan 2025 03:20:25 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3f31a19aa2dfdfc7dbfb7af6ab0ab1738412a183a90d1c98e7cc504f89fa74`  
		Last Modified: Tue, 07 Jan 2025 03:20:26 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea1c5d989f5a74d88bf74316b8ed0d5409ac48c715ae5ee838cfb5ce0c4a1593`  
		Last Modified: Tue, 07 Jan 2025 03:20:26 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaa5c6f540477b3f3f1cff1070ef75e0c275428c6c64c4ebe4f63294f191c4f2`  
		Last Modified: Tue, 07 Jan 2025 03:20:26 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:258973e86244a080771c5854d17833c4bedf00df068c3bf95ca0344e62750b60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.6 KB (492554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f82471715bcf4aea0fe77191b97b5ffa584afd5be3415cae3c545913b969375`

```dockerfile
```

-	Layers:
	-	`sha256:8b1e5d06d6642a1c540385b4ef3104be9025523419ca69dd7e264569d51ab3f8`  
		Last Modified: Tue, 07 Jan 2025 03:20:26 GMT  
		Size: 463.1 KB (463086 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a51625e387edfc9ee8907936944b5692f5bd6b0655e1aaea8c24fb284c44a6df`  
		Last Modified: Tue, 07 Jan 2025 03:20:25 GMT  
		Size: 29.5 KB (29468 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:08bf5238b74567cd9d0a52ba172f4f336ba50f6a70261a54c3f143d52b61ca53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5253566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64264c4e34fc50b7e59a3769c0297da91043bfbe3d31d42332dfa4a8d4300f9f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.4-armhf.tar.gz / # buildkit
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
	-	`sha256:9327c400cc7c63bc8696a8da86f21db1ffdb7ce43885aa521a67ab8105dd2af9`  
		Last Modified: Tue, 07 Jan 2025 02:29:49 GMT  
		Size: 3.4 MB (3363944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e8b0166e912155fa7978831718b717442802bf117592d06481335fe20d43620`  
		Last Modified: Tue, 07 Jan 2025 04:00:33 GMT  
		Size: 1.9 MB (1885032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:179c29e5b5124b5a1cc00d6584cd7e2472ce62de938c87d15df7d9d485a60913`  
		Last Modified: Tue, 07 Jan 2025 04:00:33 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9591ef3b2217746734c4b2fee2e0cf08ca57f81c16c03dd4e7d58567db046af8`  
		Last Modified: Tue, 07 Jan 2025 04:00:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b8c61413e91a8ab6fdfc275c39b7456b77158ace41ce1865390cb6776821333`  
		Last Modified: Tue, 07 Jan 2025 04:00:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309a5f1362a717f893db0f0e398f52f862d8ae2f4f6e7c6b694231024d3da2e5`  
		Last Modified: Tue, 07 Jan 2025 04:00:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a107e0277a2aeb4e3b24b9b34a1567a569a87521d51d92f681cb9c92c0dce9f4`  
		Last Modified: Tue, 07 Jan 2025 04:00:34 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3264c33eff22e94829e1da14349de937ba06a9501ba888de7e5db269e32d8b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 KB (29347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b47f1581e92581fb0e579816e6356ee1ebe2fb51b10c349b36aedd53d9ed548f`

```dockerfile
```

-	Layers:
	-	`sha256:63fbb7df428636cab86f50a7de4fa374974e92a10d63680960b4951818fcf9f5`  
		Last Modified: Tue, 07 Jan 2025 04:00:33 GMT  
		Size: 29.3 KB (29347 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:88b871ebf5f288db5fc64daf61d8b58c4a922d57c9a774f51dbfbe9406e709fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4817201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d12dd9ac4e010c308682e6ef94aadb65e65c1121568d4efaccb03e137e4c0d5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.4-armv7.tar.gz / # buildkit
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
	-	`sha256:0695ed689d581197c59573cee0b2f2ef2c3a332e0d52bbb8f0e7e0865c2d5b23`  
		Last Modified: Tue, 07 Jan 2025 02:55:40 GMT  
		Size: 3.1 MB (3091288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36814ff2ca73fcccaf61f0f2eba3040f204e0804ecf533ffbfc0977e46226ca4`  
		Last Modified: Tue, 07 Jan 2025 03:45:26 GMT  
		Size: 1.7 MB (1721326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d263def7643ebfc04fcf590f06ee4f002e4a0fcefc89f0f2a1e4f7de6b1a0a1e`  
		Last Modified: Tue, 07 Jan 2025 03:45:25 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e8ac19c8acffe421131a49300d1c591506b3fe26b61d049e8a4a590327210c`  
		Last Modified: Tue, 07 Jan 2025 03:45:25 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bea5df69b98b1cf74b29bde943f112b52283dc9e53a0df5f883e5e7b8caa9fe`  
		Last Modified: Tue, 07 Jan 2025 03:45:25 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b534874ddf1e0d92ca9b1b74b0bdd5669936003defca1fa96ec0504f89de295`  
		Last Modified: Tue, 07 Jan 2025 03:45:26 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d90ba494a93487a9227cb4a68ad47e4e22250f5b183bdbeca4fb514472ccb9`  
		Last Modified: Tue, 07 Jan 2025 03:45:26 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:26cf0e442e0c6ad11cf7c59ad59216f04ad47f0c6bfa2d5654d49c2c732742cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.7 KB (492700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12d7520d8c4fafba17b73770adc6c8905ee8b0013ff91c007e56d767461e4685`

```dockerfile
```

-	Layers:
	-	`sha256:f68eb1af3ea6f1df43820f2a550ca9ff0a466468310a753946ac63202ac7c9d8`  
		Last Modified: Tue, 07 Jan 2025 03:45:25 GMT  
		Size: 463.1 KB (463138 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:004c8ceb777d63e576de4cc78d23537ccd34f9629466cbb296f1c60cb46f1636`  
		Last Modified: Tue, 07 Jan 2025 03:45:25 GMT  
		Size: 29.6 KB (29562 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:836a954845cf078419940359cb59a34b04f2514cbcf0678293e208a4385293ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5878008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87aaa83da5f80e36159870f00c4682cddbfd49e22139662178b1baf469657af`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.4-aarch64.tar.gz / # buildkit
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
	-	`sha256:ef22e11fe7735044a1b56fc644666588aa863fb6abe827f676cb9d11ba34d993`  
		Last Modified: Tue, 07 Jan 2025 03:03:03 GMT  
		Size: 4.1 MB (4086686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94301ffc154faa5f526e33c47841f7e1f6fbac45b765e29c4179c7564d210096`  
		Last Modified: Tue, 07 Jan 2025 04:21:00 GMT  
		Size: 1.8 MB (1786738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc3e699c71a5a49f5b72e07e1aa1ab511dcfaeb2e830ffa7a8d72bbb8518ca8`  
		Last Modified: Tue, 07 Jan 2025 04:21:00 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:113b3b1cb66c6c39dee5d8c50f1bf19411884b3e64bfb06503bf685154bf8fb5`  
		Last Modified: Tue, 07 Jan 2025 04:21:00 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b30d2accfd796b18f04e50563ee787594c819925a7ada52fc91922d1067bfe`  
		Last Modified: Tue, 07 Jan 2025 04:21:00 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10c0f05d4292cf730fd33438b67a3b86810efc56065023d247152574fb4efc93`  
		Last Modified: Tue, 07 Jan 2025 04:21:01 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8587fb4394fefbf2f654abdc6f3d55179e3573c976d56012e6456c3c0636fab0`  
		Last Modified: Tue, 07 Jan 2025 04:21:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3ed1164e3c259864b3319d7338ea58d1963358a4d21a45332692cd5cd8e4c71e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.8 KB (492764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce53917b08de6600d6c4e38327f5f3302817d5c3c3b388778c9a4d3cb67948d6`

```dockerfile
```

-	Layers:
	-	`sha256:385245bfa6fd474a22bfb654289f8dc0bcf0221fbe9d110ae0138b1462bb740e`  
		Last Modified: Tue, 07 Jan 2025 04:21:00 GMT  
		Size: 463.2 KB (463166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28b4359d6d12d968065e44bb20669d3373c7fc8f5075383831d4ae937610ce5e`  
		Last Modified: Tue, 07 Jan 2025 04:21:00 GMT  
		Size: 29.6 KB (29598 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; 386

```console
$ docker pull nginx@sha256:76c824746cfb99115050b54ca7b0e1e648a8040cb32d8042c163e6817ad99414
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5420112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ef95dd6e994da6391df60550b9d31a1f468f6c00b6dfc794e9e8d13a7e02c4f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
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
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1300b040a822156c4c67686e26455802dca2906067826825eb99a38117421eb4`  
		Last Modified: Tue, 07 Jan 2025 03:20:20 GMT  
		Size: 2.0 MB (1952336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b374a9d5430e7a51fd51ed5a2352095d1c5eedd51fa7ed03589676e2c30ae680`  
		Last Modified: Tue, 07 Jan 2025 03:20:20 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:026a398fc4457420443753522c6f7efcc4d1af5e88b32e87a8b15864164ee22a`  
		Last Modified: Tue, 07 Jan 2025 03:20:20 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9d51794a9200439412a5080e028b18118679286947870da8d6e759a9030798`  
		Last Modified: Tue, 07 Jan 2025 03:20:20 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544b608f85799e2ce1c8d74f432bff68b2ac66d4c0baa15fb8c8ac1a85a0883e`  
		Last Modified: Tue, 07 Jan 2025 03:20:21 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6d558da3f511f89e102f3756d6a0d264f51fc12465a8a8b1de9caee1e2068d`  
		Last Modified: Tue, 07 Jan 2025 03:20:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:be7aa979c966291399e0f702c2c9b9c92140ccde5297a794cb6c9d0a5ea91419
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **492.5 KB (492479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c6c966b077ecce737e877e275ae4230572bc04ba97b64ba3be23bc023bd3755`

```dockerfile
```

-	Layers:
	-	`sha256:64f43967e981a9a08044899d22b854b0c972e99397362a42debacbacb7279a51`  
		Last Modified: Tue, 07 Jan 2025 03:20:20 GMT  
		Size: 463.1 KB (463051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d03309a95fff68ef306097aec6c8e327f837ac2f58a7f94f15bb2009705ab32`  
		Last Modified: Tue, 07 Jan 2025 03:20:20 GMT  
		Size: 29.4 KB (29428 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:d0e25445b18346061545e2785255e0cb928f76396bc9d1518ec46dc3e74a51e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5516517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb298034183f5fb2c7fe62a240042923c12330cc4869a7e0de3946edc611014`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
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
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea52955eda00e1680b58ab43645d16b764c6199273e041ceca56faa267098182`  
		Last Modified: Tue, 07 Jan 2025 03:53:11 GMT  
		Size: 1.9 MB (1943203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:005b977ad2011fde9a9e2c3775eb20767895678bf999fbe326de83e5f93caa8f`  
		Last Modified: Tue, 07 Jan 2025 03:53:10 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf63e685988f5010b1407237077d58010972d0b9a50873f98b100670f7ac98db`  
		Last Modified: Tue, 07 Jan 2025 03:53:10 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3845514290be2dc602ff61ae071aec9788ffded280042531188373b5690a6d16`  
		Last Modified: Tue, 07 Jan 2025 03:53:10 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a956beea5961814fb0983cb5eaaea62143fc0b2718911cfa306307e58956a170`  
		Last Modified: Tue, 07 Jan 2025 03:53:11 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6654f8470611f7ad5579544257f7c0066b8e98b33c0083e1eec30b01fb06aadf`  
		Last Modified: Tue, 07 Jan 2025 03:53:11 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:fd36960b2999760eca742ed7a6a31de43a740219eabf68d9233980932c8a3ebf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 KB (490707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:764d6f7d96d47e1187344b53bc5dc133adc57453c01262f683cd9326546ebc13`

```dockerfile
```

-	Layers:
	-	`sha256:120f8706ec2eeabc1220530da26989767bad5f6e5aa78b86dea4575b919e553e`  
		Last Modified: Tue, 07 Jan 2025 03:53:10 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de3b7544a21ce5f3a665890dd84e777a0cf50195269d532e96e89f1716f6d24d`  
		Last Modified: Tue, 07 Jan 2025 03:53:10 GMT  
		Size: 29.5 KB (29526 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:5502b2a7d1842b0cfd0f293965147a59c79521da20f9ffa01f9d06bcab3c70e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:232f39198a9955b169ad28fc8c67a5d3a429043533c5d2bd6532d4dec886c6c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.4-riscv64.tar.gz / # buildkit
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
	-	`sha256:bb004d8f7711d1f01f66ee3b1754326effc166c60f63ee7f0748d2ea817676c4`  
		Last Modified: Tue, 07 Jan 2025 02:33:45 GMT  
		Size: 3.4 MB (3361534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33c3b4efa61b4154592b35f428613c470aaf3a392e14045ae0d2588c325b4faa`  
		Last Modified: Tue, 07 Jan 2025 07:39:20 GMT  
		Size: 1.9 MB (1923772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7513c7b7d7b8c5acecee80fa17d070a232ef12849c48ccdcfed2246ae80f014e`  
		Last Modified: Tue, 07 Jan 2025 07:39:20 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc82b528bbee2eab33a35b7f8b3724d91d2ef3dae6ea53f785fbfb6a91f8b85`  
		Last Modified: Tue, 07 Jan 2025 07:39:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae58bfe1837a8f14b8570baa0a5fd63bada187ecc6787d049f36e583158d6815`  
		Last Modified: Tue, 07 Jan 2025 07:39:20 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3944c14c61b1b876c2049300aa3506f2377be3cdf687125c0e6995dcf6d6873d`  
		Last Modified: Tue, 07 Jan 2025 07:39:20 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98d135fb8cb10efe87aa7578f241733f160805756a01b96062bea93234dc7a12`  
		Last Modified: Tue, 07 Jan 2025 07:39:21 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:98defa67fe266d5a203da73a10f0890e59e7b2159b673c528869da72ef431484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 KB (490702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38f68691343cf72a4b7ff8e7b9aeae510786c5b8cbbe4c9b2983a1e483b2fbb0`

```dockerfile
```

-	Layers:
	-	`sha256:6d7309758d0c07d1bce0bf413fc94b04b2a569929487ee84ef182bf1e09a8298`  
		Last Modified: Tue, 07 Jan 2025 07:39:20 GMT  
		Size: 461.2 KB (461177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94fbdcb1b0718f9347a5086af7bfe2743c9695fb6742becfbb51a9079e3646d3`  
		Last Modified: Tue, 07 Jan 2025 07:39:20 GMT  
		Size: 29.5 KB (29525 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; s390x

```console
$ docker pull nginx@sha256:90700c59492e7f63a1e6490b681d102fdbddb9c0e8864bdecbe45de67cb5747e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5438552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d0545c1406182ac0930dba9c9129040e195e319de489a0b8fdc6ad7b5d61180`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 15 Aug 2024 00:20:26 GMT
ADD alpine-minirootfs-3.20.4-s390x.tar.gz / # buildkit
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
	-	`sha256:2ed16bdf68dac880df118dfa3d21d44652bc18382729359f97297fa5998086cd`  
		Last Modified: Tue, 07 Jan 2025 02:32:49 GMT  
		Size: 3.5 MB (3459179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b83b215ddb6e38f1c0d8138955541c9ede0544bee70e50b39dc420e928b2e16a`  
		Last Modified: Tue, 07 Jan 2025 03:48:55 GMT  
		Size: 2.0 MB (1974784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eb110f41c21c885b7305ad3dca3f3b77ca52836a880b68bb50a38095b76896b`  
		Last Modified: Tue, 07 Jan 2025 03:48:55 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09cafc32440b086f697d97b832e32c619119f862ff8aa25c6d971af30ad4fb1`  
		Last Modified: Tue, 07 Jan 2025 03:48:55 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f051dd9ba1739dcfe789af4ccc6f83ae690ff6feaabf087a0004555ef90b2da1`  
		Last Modified: Tue, 07 Jan 2025 03:48:55 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f928ef943ebf222dd4a6d4de2ecbda33073b668b3b116abf9090d09692d1fb9c`  
		Last Modified: Tue, 07 Jan 2025 03:48:56 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31192b096a9d9e554cfb04c98105bd195fcaba89c21632260a2f7cd974b9b267`  
		Last Modified: Tue, 07 Jan 2025 03:48:56 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:16e876818df561a62dec097bec0ce853d8cde3e479ed90f9277e2991e74f4b4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.6 KB (490605 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a82c437f298079bc1cfa00f058a7e522962a6c4f1272a564ef590356642821aa`

```dockerfile
```

-	Layers:
	-	`sha256:0897d133cb851845e5778d319fabd86c27d5e8f1db35dc6f6944d06af9eec905`  
		Last Modified: Tue, 07 Jan 2025 03:48:55 GMT  
		Size: 461.1 KB (461135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:318d3120edf8d52baeafdf2940472c5fd420b6ea9c682a03e2426f54041c01af`  
		Last Modified: Tue, 07 Jan 2025 03:48:55 GMT  
		Size: 29.5 KB (29470 bytes)  
		MIME: application/vnd.in-toto+json
