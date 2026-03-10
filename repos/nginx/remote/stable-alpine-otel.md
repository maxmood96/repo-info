## `nginx:stable-alpine-otel`

```console
$ docker pull nginx@sha256:fd98de57d7fa60d20a2d95386120ca9b6752d1b2cd79732c9b33c3dd838e8e44
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:stable-alpine-otel` - linux; amd64

```console
$ docker pull nginx@sha256:4ab2c57867e7e3854160665bf5980d08364dfd45760e448093df2f1e08fb694d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42692399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1a93ed6b326a848a825c6e06f8e9182899137a442d50d57c6872dc3d58f71c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:04 GMT
ADD alpine-minirootfs-3.23.3-x86_64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:04 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:51:53 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:51:53 GMT
ENV NGINX_VERSION=1.28.2
# Tue, 10 Mar 2026 20:51:53 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:53 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:53 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:53 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:51:53 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:53 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:53 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:53 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:53 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:51:53 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:51:53 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:51:53 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:12:01 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:12:01 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:12:01 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:12:01 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 10 Mar 2026 21:38:28 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 10 Mar 2026 21:38:28 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:589002ba0eaed121a1dbf42f6648f29e5be55d5c8a6ee0f8eaa0285cc21ac153`  
		Last Modified: Wed, 28 Jan 2026 01:18:09 GMT  
		Size: 3.9 MB (3861821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd53180853addc043d0403ab470dc0cc3d7c559afb68767fdce8bc0ab427a37f`  
		Last Modified: Tue, 10 Mar 2026 20:51:58 GMT  
		Size: 1.8 MB (1833768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7687623c32112cd1fe0d193dfab517acb0071abb8e13d6baacd98b3c143e62f8`  
		Last Modified: Tue, 10 Mar 2026 20:51:58 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c747420fb6ab2e2279dd909937d4251b4f8a2993adeded7850e88421a1301c34`  
		Last Modified: Tue, 10 Mar 2026 20:51:58 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54bb357c94ab61ac3840caff71a7564f71644285da39ceed5983082a66390520`  
		Last Modified: Tue, 10 Mar 2026 20:51:58 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157c88569e8335368269719fbdc2bcb9323b757c27983e5c5e0298f6beadea5`  
		Last Modified: Tue, 10 Mar 2026 20:51:59 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7a9fbefb9250566928a7bf5619c1a5c491b9f3928cd209f07753cde1bf416b5`  
		Last Modified: Tue, 10 Mar 2026 20:51:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43f6fe9104001872e4b8e56421362ef8a2e9379e69184347a64fdb1185f2ce3b`  
		Last Modified: Tue, 10 Mar 2026 21:12:09 GMT  
		Size: 20.2 MB (20240627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c5706cabc2ddd5f29174402ab2521e3f87198a18db19e83a897dbebe7c360e9`  
		Last Modified: Tue, 10 Mar 2026 21:38:41 GMT  
		Size: 16.8 MB (16751590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:b0f57786d3574896ab499579624094d67343d2785e9283145b2714f7e012b4c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1094964 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b594119e1bdb108e486749be91dd26e98efa195074e858e86a116bc43317124`

```dockerfile
```

-	Layers:
	-	`sha256:ff31e878e678417c134ae6b885363861f3a737e342e276fc0031c66e9b95983c`  
		Last Modified: Tue, 10 Mar 2026 21:38:35 GMT  
		Size: 1.1 MB (1074702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27816aa4abc4186a04b40efc1a3b87503ea57b5f609151a6f83a49d306203f58`  
		Last Modified: Tue, 10 Mar 2026 21:38:35 GMT  
		Size: 20.3 KB (20262 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:fc4b47961b89b85ba044feb97a02bd0065824461a7088510c4d0f982f947e6ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41488590 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a513ff148486b1ed2dbd33c62ef59c1aa3257dc81c00b52e7091df3d5c563a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:09 GMT
ADD alpine-minirootfs-3.23.3-aarch64.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:09 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:52:10 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:52:10 GMT
ENV NGINX_VERSION=1.28.2
# Tue, 10 Mar 2026 20:52:10 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:52:10 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:52:10 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:10 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:52:10 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:10 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:10 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:10 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:52:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:52:10 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:52:10 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:52:10 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:12:43 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:12:43 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:12:43 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:12:43 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 10 Mar 2026 21:38:24 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 10 Mar 2026 21:38:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:d8ad8cd72600f46cc068e16c39046ebc76526e41051f43a8c249884b200936c0`  
		Last Modified: Wed, 28 Jan 2026 01:18:15 GMT  
		Size: 4.2 MB (4197091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b38294787f335b56057503805b73c325bafa46df3fd28e9ae8e51520c4edf04`  
		Last Modified: Tue, 10 Mar 2026 20:52:15 GMT  
		Size: 1.9 MB (1852819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97fce410b87e0695047e27c06a23cfa7a7489c6e93fe5ff11e36d55cba2e43c`  
		Last Modified: Tue, 10 Mar 2026 20:52:15 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3c2740a816d74452653e75dfd9322d263869791963e6aea6bc49b8d1df4fcc`  
		Last Modified: Tue, 10 Mar 2026 20:52:15 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb415bd1d1356c52a81e12534ab9b7e949037cc078a2eaa1030ad5cc9735683`  
		Last Modified: Tue, 10 Mar 2026 20:52:15 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8e8bc3e2dee063852f9686bcfec81573b30065ac652baba97701098ba1565d1`  
		Last Modified: Tue, 10 Mar 2026 20:52:16 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946b8edb1505723b25298706c0527db56435477c1d6c12a17544ba257442c693`  
		Last Modified: Tue, 10 Mar 2026 20:52:16 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c14b98587eab11835148c4ac6c3ff08c143a6871d010ffa30935265dae111c4`  
		Last Modified: Tue, 10 Mar 2026 21:12:50 GMT  
		Size: 19.7 MB (19711261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed0d7c53454cccd8a44a92e60615a888c7f6ef90aa341f08fcfa80b968261db3`  
		Last Modified: Tue, 10 Mar 2026 21:38:31 GMT  
		Size: 15.7 MB (15722823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:20c4adc8c06dec15f632183b44999700fb4228b188bb7101b71b7bb66d868a87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1094521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738e7f91afd34f5600dc0e30240daa892899d213a66852eeadb41ac992396f29`

```dockerfile
```

-	Layers:
	-	`sha256:820fc79bba22583026174d7136cf33415e7b2242e9955bbc3d0fe2499984b97c`  
		Last Modified: Tue, 10 Mar 2026 21:38:31 GMT  
		Size: 1.1 MB (1074132 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e6ce575674a3fa05f719acdee5cc8c39007ff3e1a590489242d1884101859e3c`  
		Last Modified: Tue, 10 Mar 2026 21:38:31 GMT  
		Size: 20.4 KB (20389 bytes)  
		MIME: application/vnd.in-toto+json
