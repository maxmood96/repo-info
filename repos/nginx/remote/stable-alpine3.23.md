## `nginx:stable-alpine3.23`

```console
$ docker pull nginx@sha256:87add5f1c1dae6da99a45966b2689b707580bc330065fa03312964b4242d7a99
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

### `nginx:stable-alpine3.23` - linux; amd64

```console
$ docker pull nginx@sha256:0c8a74b863b202a8e9ce8b2f97cc8bf96bc573206d46c2c469d507095dd2c77e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25940809 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43a775095fde460e747cc4799d2060c1953d588f6b896443051acccab1bb355f`
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

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:bde9989da06778d2c97c8f922b474df312353819b838cbde847aa64621ffc9e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.2 KB (907207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:810c7ccd7dc6fe9615537d82c9c0bdff7394fdfc7589bae8dd79f631896bc29c`

```dockerfile
```

-	Layers:
	-	`sha256:e149c938737a3570af3f8cbe797f513586fd8eb214aa2926748a45318aacdefe`  
		Last Modified: Tue, 10 Mar 2026 21:12:08 GMT  
		Size: 885.9 KB (885912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a270627d13ec2d2bd018150611040ead1b7a75790b36b6033bffdfea8fa32019`  
		Last Modified: Tue, 10 Mar 2026 21:12:08 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; arm variant v6

```console
$ docker pull nginx@sha256:dbfc6d6ea9b6ab767f9b9ec6ad293e407d55b6c97efe8707d1740150ab6c83cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.7 MB (19650731 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e46b854d76ec7bd2652bfc8ac8f88eecb624dcea36c1a00cfd3cfcd184115b79`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:52 GMT
ADD alpine-minirootfs-3.23.3-armhf.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:52 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 21:08:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 21:08:31 GMT
ENV NGINX_VERSION=1.28.2
# Tue, 10 Mar 2026 21:08:31 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 21:08:31 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 21:08:31 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:08:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 21:08:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:08:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:08:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:08:32 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 21:08:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 21:08:32 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 21:08:32 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 21:08:32 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:45:51 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:45:51 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:45:51 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:45:51 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:f067a9ad7b3a4e3b687105344f6ad0934a0623c4359c2d841a3d4fab27e26060`  
		Last Modified: Wed, 28 Jan 2026 01:17:56 GMT  
		Size: 3.6 MB (3569821 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398001c55a515100230b9d74edf06ffec3ca4a249fbe39bc7b1b7cff352f2248`  
		Last Modified: Tue, 10 Mar 2026 21:08:36 GMT  
		Size: 1.9 MB (1878724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5ed7fe53fc1bfeade73f193bb0720614a7a24b0bea421398e4cbb719c7968e4`  
		Last Modified: Tue, 10 Mar 2026 21:08:35 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c498aad8dfc5552291e3183babbe7e0969ca5edf7e19cbcf7ff820a3e7dd0f50`  
		Last Modified: Tue, 10 Mar 2026 21:08:35 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247bbf10fa73a956e671ec49d7db7d55c1a5df011e8612b4ef4cfb6c8a5c72d1`  
		Last Modified: Tue, 10 Mar 2026 21:08:36 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d64a051fc8f7761989068f38592ab66f15aea9b4f1585b9d49215b150ecd0075`  
		Last Modified: Tue, 10 Mar 2026 21:08:37 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:915f78556ee7ff950795bc1907168ddc0d01c79d94cbf00e3a5ea08470414660`  
		Last Modified: Tue, 10 Mar 2026 21:08:37 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d18b434d18f16305b7cda6c586b3cacc88c62dcbcaa038165845855938053b9`  
		Last Modified: Tue, 10 Mar 2026 21:45:56 GMT  
		Size: 14.2 MB (14197590 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:024af81181d01112e40af893655c66b220430013438a4ab2b737aeaa781b54fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 KB (21176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf1640e7fa943a5019a7a77860f370ecec67c129228a1d27e8c2a118095447ba`

```dockerfile
```

-	Layers:
	-	`sha256:4c3cfc9134e288bf1d0cb676e342a737e9cc63536cf9378b4800dae0d411fbb8`  
		Last Modified: Tue, 10 Mar 2026 21:45:56 GMT  
		Size: 21.2 KB (21176 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; arm variant v7

```console
$ docker pull nginx@sha256:8d85144382f9836eb97060b2ffd092946b6cbfcaecb0debd04c6010c925e120c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.6 MB (21629908 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3985f92367c22c14de2b4c9946460ef3d7ed130d5d8e14697d71c53c162b5002`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:44 GMT
ADD alpine-minirootfs-3.23.3-armv7.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:44 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:54:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:54:45 GMT
ENV NGINX_VERSION=1.28.2
# Tue, 10 Mar 2026 20:54:45 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:54:45 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:54:45 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:54:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:54:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:54:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:54:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:54:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:54:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:54:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:54:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:54:45 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:15:55 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:15:55 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:15:55 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:15:55 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:7ed661450d9b41ba25f81f6ef8649bb379f47471d21c4898a8a6a3e11b819220`  
		Last Modified: Wed, 28 Jan 2026 01:18:50 GMT  
		Size: 3.3 MB (3281724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3855a24ec3d94e6eb696397a8ddffdbb62bd68f49c5b19be35beab4a826c485`  
		Last Modified: Tue, 10 Mar 2026 20:54:50 GMT  
		Size: 1.7 MB (1705113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e4d6e95630e8d2955036da82586780940c91b6dadb7fe4aeacd55953b88d34d`  
		Last Modified: Tue, 10 Mar 2026 20:54:50 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77182d5ce2ab8bc39a144f329ba42ebc437b9a12a58ccf665e5e166722c66747`  
		Last Modified: Tue, 10 Mar 2026 20:54:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53d8433f75b6b00d0d707782811bd29277be55035ddda9ee9153f45e649044ce`  
		Last Modified: Tue, 10 Mar 2026 20:54:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e09e0f6bc877cc06d031ac60f4b0a2bba7a948172de4f5a4aff0fa0b41fa2ce`  
		Last Modified: Tue, 10 Mar 2026 20:54:51 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0395fdb2b9f31527317792ab439dd6b72d804492abdda2c8d526e69e83316ac`  
		Last Modified: Tue, 10 Mar 2026 20:54:51 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaf4dd9283504c2ff5d21128afe6ffbf344aab50e4036c9fa9b1d87f1604d1f`  
		Last Modified: Tue, 10 Mar 2026 21:16:02 GMT  
		Size: 16.6 MB (16638475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:13a9765e5f2b3e63c27d2e5083f4dfa9fa127e0c0bc4767c3a873d8347c7f674
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.7 KB (906705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5181207a5b994566b8bd5a73961817a87c444ad7f412276edc30710ce625e611`

```dockerfile
```

-	Layers:
	-	`sha256:3196a2a30e40f8dfdd61a36e2015f5ece79ae05c24f8b0a915ed51de41a53c3b`  
		Last Modified: Tue, 10 Mar 2026 21:16:01 GMT  
		Size: 885.3 KB (885314 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b22786c526cdb6ed2d92e8afdfd83681db6f48afb192523c94578c00248e1b2b`  
		Last Modified: Tue, 10 Mar 2026 21:16:01 GMT  
		Size: 21.4 KB (21391 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:7bff6f17bf625958486d1beb182abbce4ac22013265a8ec8c3836ea566028310
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25765767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf280afcb57d1269dee9097230e104260d67de6be94156082e10504f954dc2e`
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

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:500441e5adb430c6d7ed092acc6447cf1b72a88ea39091afa458f7f91185a561
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.8 KB (906765 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ba866fcfd428cd8de19b33cf48ee96b0e598bc7476c711871fcf9ffcbc91b5a`

```dockerfile
```

-	Layers:
	-	`sha256:938f212607b29b7bb9dec3c41db0bb903b168fb1a4dabdd7cf1ab5a2f0a77274`  
		Last Modified: Tue, 10 Mar 2026 21:12:49 GMT  
		Size: 885.3 KB (885342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a48647e3c776d9b17a888905e9d7e6584a333cde234ef3a4d6a0ed5b1dcb659`  
		Last Modified: Tue, 10 Mar 2026 21:12:49 GMT  
		Size: 21.4 KB (21423 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; 386

```console
$ docker pull nginx@sha256:a7f30349ff7620cd08e4d9e676e19ce268bf1b7bd1f63c5b9202016fa5a7860a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.3 MB (25290372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40603950cfc0756880bc10ac87590c380068984b7a14ef1251662e448688f870`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:18:11 GMT
ADD alpine-minirootfs-3.23.3-x86.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:18:11 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:53:27 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:53:27 GMT
ENV NGINX_VERSION=1.28.2
# Tue, 10 Mar 2026 20:53:27 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:53:27 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:53:27 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:53:27 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:27 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:27 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:27 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:53:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:53:27 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:53:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:53:27 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:15:52 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:15:52 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:15:52 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:15:52 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:18bdec7eea78464ecf9b88f4ec630eaeb694ea1c0101ecd9c20eda20c9065e23`  
		Last Modified: Wed, 28 Jan 2026 01:18:16 GMT  
		Size: 3.7 MB (3686998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:784edda663bcb1dc54ac1fae3a29386990ddf116f7df7fd6d2c1dff6eafd8e56`  
		Last Modified: Tue, 10 Mar 2026 20:53:33 GMT  
		Size: 2.0 MB (1960362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebf8d21fc51219e13cbf4a7bda58f1102898e28a005dcc68ba8dc8d4f8a5f538`  
		Last Modified: Tue, 10 Mar 2026 20:53:33 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6443d822a3ffef2abfa8a04e206d63b6fa5da5d8a6b6505823b5bb0a6682367b`  
		Last Modified: Tue, 10 Mar 2026 20:53:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7e2257101f9d94c7c99d5d9bd9d255ef261b128a5d6f903aa06d03d492157ad`  
		Last Modified: Tue, 10 Mar 2026 20:53:33 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309adbc22ac4d8a9425387ca67a3a852c2258c071eb3f01b1415a9dcad79059d`  
		Last Modified: Tue, 10 Mar 2026 20:53:34 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:946b1ab0528dda13048aac44120e97a25e248912dd42ddf6a3fd78cc2d7b0bc0`  
		Last Modified: Tue, 10 Mar 2026 20:53:34 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c29341bbbe0e79032df2a0846d5568aab358edfa353fdf19102dfce7eefc408`  
		Last Modified: Tue, 10 Mar 2026 21:16:00 GMT  
		Size: 19.6 MB (19638416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:146f708acd9b3c06692818c167fa7d9083cf1bb08e17014cf513cd8e2cf2808d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **907.1 KB (907130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2d81754b78bdb9d7c9c6f325a3439132cf08b13669ec8576e8a3c86e0abf52`

```dockerfile
```

-	Layers:
	-	`sha256:56293cadbeb2753c622cfda4a3642d7d6cc1fdb17977c62ba84ca9ce2bc89f6a`  
		Last Modified: Tue, 10 Mar 2026 21:15:59 GMT  
		Size: 885.9 KB (885877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35df53ad67ccc987ed314025b413933a741d8a6a80ce77b38f1316f3f422d497`  
		Last Modified: Tue, 10 Mar 2026 21:15:58 GMT  
		Size: 21.3 KB (21253 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; ppc64le

```console
$ docker pull nginx@sha256:cecd3bfa7016b554f7a48cc273fee28cdc9839ff898d0768eb97b6967b28dc8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.3 MB (26319757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2885683c2cc9235cfa2b94f009a21e5c81131167a12db6e25ed6a44f75f50c7a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:01 GMT
ADD alpine-minirootfs-3.23.3-ppc64le.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:01 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:51:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:51:48 GMT
ENV NGINX_VERSION=1.28.2
# Tue, 10 Mar 2026 20:51:48 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:48 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:48 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:51:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:50 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:51:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:51:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:51:50 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:16:24 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:16:24 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:16:24 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:16:24 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:532f7d227cfd697fe6a6f7bfe8c0cc7baa9d99d3d41d50d9b6394fdb6322f4aa`  
		Last Modified: Wed, 28 Jan 2026 01:17:23 GMT  
		Size: 3.8 MB (3829643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:078d548e464e0bc196a6ede94b89117b007ab48473c52ef637cecf74a3b6b0bf`  
		Last Modified: Tue, 10 Mar 2026 20:52:04 GMT  
		Size: 2.0 MB (1984228 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1e08480a46cfd715e9619dc01468e573cb64bf727f6acc59669b383b4e5eda5`  
		Last Modified: Tue, 10 Mar 2026 20:52:04 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fdd4dfa31dbf98452b84b13d05e0bc47b0d3b772d22e5e2d758ed25f84f7f71`  
		Last Modified: Tue, 10 Mar 2026 20:52:04 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d93c8fb2ed84b1c0b29dc1469699a626c0653b751e3e75a6fa17402b0eeae727`  
		Last Modified: Tue, 10 Mar 2026 20:52:04 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb686ae5f8a43d751874f6f3ec1fb509b895e6e44baf5507d7932ec2caa9e520`  
		Last Modified: Tue, 10 Mar 2026 20:52:05 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c00d9293decfe9609b5dfff345f423c6727632004f69ae99ee80d490dcb208`  
		Last Modified: Tue, 10 Mar 2026 20:52:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e42a745f3ad437e8f7b47cf04397d2871eb0686eefdb9ca79b83f33fde2f1f`  
		Last Modified: Tue, 10 Mar 2026 21:16:37 GMT  
		Size: 20.5 MB (20501294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:d6a19eb0b14f1e81e752e33878ffa910dcd6afbbfff2d94e4e45dc94bdeb7da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.7 KB (906658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:737a08dc96afb78cd419a889667ac593006f625c1b93236b7dfc64c1fe051421`

```dockerfile
```

-	Layers:
	-	`sha256:3d4097bc903b66aa2b473d4423d42a62357492b671d8f06cbcf058ba800ec7b1`  
		Last Modified: Tue, 10 Mar 2026 21:16:37 GMT  
		Size: 885.3 KB (885307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:632577e6e7054709cd37bf7771eeef009397e8602cc8f84846918e2d8e88e2ed`  
		Last Modified: Tue, 10 Mar 2026 21:16:37 GMT  
		Size: 21.4 KB (21351 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; riscv64

```console
$ docker pull nginx@sha256:14ac2a25e4d828967da687f7b01c1ea9278af8e0a28b7dfd8f09fac3dd76b502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23464388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97ef7b5d1761caf3de6fe437eecb7753cf5749008d61bce2fbb2cbb154036262`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 03:47:28 GMT
ADD alpine-minirootfs-3.23.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:47:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Feb 2026 03:57:43 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 06 Feb 2026 03:57:43 GMT
ENV NGINX_VERSION=1.28.2
# Fri, 06 Feb 2026 03:57:43 GMT
ENV PKG_RELEASE=1
# Fri, 06 Feb 2026 03:57:43 GMT
ENV DYNPKG_RELEASE=1
# Fri, 06 Feb 2026 03:57:43 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 03:57:43 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Feb 2026 03:57:43 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 03:57:43 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 03:57:44 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 03:57:44 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 03:57:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Feb 2026 03:57:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Feb 2026 03:57:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Feb 2026 03:57:44 GMT
CMD ["nginx" "-g" "daemon off;"]
# Sat, 07 Feb 2026 23:02:28 GMT
ENV NJS_VERSION=0.9.5
# Sat, 07 Feb 2026 23:02:28 GMT
ENV NJS_RELEASE=1
# Sat, 07 Feb 2026 23:02:28 GMT
ENV ACME_VERSION=0.3.1
# Sat, 07 Feb 2026 23:02:28 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:9da5d16b2a566416844fd0c62fa81165037aa0b7f154a5c1f58f06412739471c`  
		Last Modified: Wed, 28 Jan 2026 03:48:00 GMT  
		Size: 3.6 MB (3585287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43cbe5081648aa5fb38d0c7fa3d634b854e085a4e6f988d564b275af94166759`  
		Last Modified: Fri, 06 Feb 2026 03:58:09 GMT  
		Size: 1.9 MB (1879254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5cd65d3e997e8de6220bd66b2e8ab53b46770b6041d1a002962852b3cacaa9`  
		Last Modified: Fri, 06 Feb 2026 03:58:09 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6229aba6575c2a60bcbbb5f39b8c0f7f33832216b6e8242e1c77f6b26bb89d77`  
		Last Modified: Fri, 06 Feb 2026 03:58:09 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68a454cbea55d4d0b9af486100851310c0c6be737a83701279c1af46000a5690`  
		Last Modified: Fri, 06 Feb 2026 03:58:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9d4fbd49894776e09d6f88e023b9a9a95f869baeaa61b0fcffc6c1617fd1342`  
		Last Modified: Fri, 06 Feb 2026 03:58:10 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f159ec8bdba49ad6e667968c88628d1fba23f3ec3e74385f8bb6915b25d4d739`  
		Last Modified: Fri, 06 Feb 2026 03:58:10 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6943523b582ce01cf58e1924b33f52f8c8a6d3c5d07c804e2672f3b17c704941`  
		Last Modified: Sat, 07 Feb 2026 23:03:18 GMT  
		Size: 18.0 MB (17995245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:cf058a16fc4d498ab007411eeb39b59569404342e32563cb0444e0ab5cef4974
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.7 KB (906654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a05bb2a5774b82699a3b772169a4f8599be95dbaea12f73644b8d4d6b8233770`

```dockerfile
```

-	Layers:
	-	`sha256:2ce3d9d2140ee10cb07017a107542f7f6586d517bfbf6e27d8933e6e522fad6d`  
		Last Modified: Sat, 07 Feb 2026 23:03:16 GMT  
		Size: 885.3 KB (885303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f0e5d8008541e09b1e823aafe154d0d1aa979a2bbd42e670fffc0285043078c7`  
		Last Modified: Sat, 07 Feb 2026 23:03:15 GMT  
		Size: 21.4 KB (21351 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23` - linux; s390x

```console
$ docker pull nginx@sha256:f29e10f0149351fc5f32095100cf89ae08a26a2681861d330cabd6779ed09e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26095192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8d279f396f275b28f2f9037a8fc1d1a22acd08326614367b25e109100f483d4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 28 Jan 2026 01:17:06 GMT
ADD alpine-minirootfs-3.23.3-s390x.tar.gz / # buildkit
# Wed, 28 Jan 2026 01:17:06 GMT
CMD ["/bin/sh"]
# Tue, 10 Mar 2026 20:51:34 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 20:51:34 GMT
ENV NGINX_VERSION=1.28.2
# Tue, 10 Mar 2026 20:51:34 GMT
ENV PKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:34 GMT
ENV DYNPKG_RELEASE=1
# Tue, 10 Mar 2026 20:51:34 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 20:51:34 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 20:51:34 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 20:51:34 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 20:51:34 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 10 Mar 2026 21:13:40 GMT
ENV NJS_VERSION=0.9.5
# Tue, 10 Mar 2026 21:13:40 GMT
ENV NJS_RELEASE=1
# Tue, 10 Mar 2026 21:13:40 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 21:13:40 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"ef4545c05b1632a056482e3dbb47bb5d7393238318db3491e8bb308218cdb5f32dbb2ac73509097ac2426fd73270bc97836843a8b1846a396fd94e60826f7e3f *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:623c99520afcb8c68e21bd22d3bc252ae348c276fb9c45a79aeccb4caf2b8d9f`  
		Last Modified: Wed, 28 Jan 2026 01:17:15 GMT  
		Size: 3.7 MB (3725333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f4c8a1cba393ffd777772f50a2b5c04e096eeab25c9bf92764dc01a416a9fe3`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 2.0 MB (2009369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:413ae54b69f26f91b04ba97f631a509614176c5ea36f780fadbd82844163c936`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7091df6db2b6aa981c5866b1914abc09e266fe0a824ba4dd30b35ebba95fbd35`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c979dbcbf13a221da9c1ba4a6b7110bd86cb1435f87b65334ad5027a9bd02f`  
		Last Modified: Tue, 10 Mar 2026 20:51:44 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2553f1020ff70f7481bf5fe9e0d1bc2918885a984bab604f2f14fe180b60847`  
		Last Modified: Tue, 10 Mar 2026 20:51:45 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6a16ebd9d06f24d58c51efcbfec20f3239dd17edfb34cdd258be6f13da73a79`  
		Last Modified: Tue, 10 Mar 2026 20:51:45 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef16de39f3112b96471d85807422d939c87428827d8b5564ec1cf05f8a6edc1`  
		Last Modified: Tue, 10 Mar 2026 21:13:53 GMT  
		Size: 20.4 MB (20355894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23` - unknown; unknown

```console
$ docker pull nginx@sha256:a3da72a18bebbf212e61b8fdc7941b5c351d344d715122c8b294e2b678d6929d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **906.6 KB (906556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b34732577b55a1aae7f6fdce1cf7c0e39dbb63bdd336a29a1126f933c0c515f1`

```dockerfile
```

-	Layers:
	-	`sha256:04f24ed88169c3a37edf9b4854dac916917fde336e4ec88c733b236d99a620ee`  
		Last Modified: Tue, 10 Mar 2026 21:13:52 GMT  
		Size: 885.3 KB (885261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35325dcd5b2a03d5e29c3f23a0e2ce2180d83c178985e17cf752f462402f1782`  
		Last Modified: Tue, 10 Mar 2026 21:13:52 GMT  
		Size: 21.3 KB (21295 bytes)  
		MIME: application/vnd.in-toto+json
