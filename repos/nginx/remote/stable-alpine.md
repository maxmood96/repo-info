## `nginx:stable-alpine`

```console
$ docker pull nginx@sha256:d812cb6d2dbf077efc25d31324ae3057416f4689e6f72c76aea34a251194bd1a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
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
	-	linux; s390x
	-	unknown; unknown

### `nginx:stable-alpine` - linux; amd64

```console
$ docker pull nginx@sha256:daaa4efb3bb69b5c32a99a6bf17a88b94d793dcef4155e25966b3fc939f2e8f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20438818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aad9d2c57addc25b3941723ed63bfbf78ff0628f1179f639ed9ed647bfbbda78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/73d6839714a2.tar.gz                 && PKGOSSCHECKSUM=\"95d513d058493d60cba5a6bb328dc3c3e75ea115cf248a64bd921159e11c6fc87d33c7f058562c584fe440a219b931d53fd66bd4c596244b54287b62979834db *73d6839714a2.tar.gz\"                 && if [ \"\$(openssl sha512 -r 73d6839714a2.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 73d6839714a2.tar.gz                 && cd pkg-oss-73d6839714a2                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/73d6839714a2.tar.gz                 && PKGOSSCHECKSUM=\"95d513d058493d60cba5a6bb328dc3c3e75ea115cf248a64bd921159e11c6fc87d33c7f058562c584fe440a219b931d53fd66bd4c596244b54287b62979834db *73d6839714a2.tar.gz\"                 && if [ \"\$(openssl sha512 -r 73d6839714a2.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 73d6839714a2.tar.gz                 && cd pkg-oss-73d6839714a2                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3129a53fcac06e353923c712ac89f1f615351d6caebeff843f8541dc108e5f62`  
		Last Modified: Mon, 06 May 2024 17:57:55 GMT  
		Size: 4.0 MB (3985411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c6306186bfa8d72a599f9a6681170f6fc49ae71e550ed91d5e5f29de5396dd`  
		Last Modified: Mon, 06 May 2024 17:57:54 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:097adf26662dbcb8353dbab98f92447c8fcc8dd10e6b3e7277ab15c4f07020db`  
		Last Modified: Mon, 06 May 2024 17:57:54 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b4ece6aebb1921391be4df28d47f78830882996352fe80d453ebd7c26e58f9`  
		Last Modified: Mon, 06 May 2024 17:57:55 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7101c757445269bb0ba0f116a908a9855835bd10f03033a6a25839de99bf6f49`  
		Last Modified: Mon, 06 May 2024 17:57:55 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98679bd100072c2c5ab40d385bcfaf94fcb1e98d05121db1a5273bf5c52ac448`  
		Last Modified: Mon, 06 May 2024 17:57:56 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1a0e0d8fc1d10549523ad6e8c172c18bb45a23a86238dc3eca377a5336485b1`  
		Last Modified: Mon, 06 May 2024 18:55:42 GMT  
		Size: 13.0 MB (13040097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:7f100ce34e4ca978e91d9ca3d165726111ada6235407594d17e38481d055cfa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1250448 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:202e54a498baa8ef034435ef828e62b6de3c691ee5e29b8570e0cde2e0c6d677`

```dockerfile
```

-	Layers:
	-	`sha256:456b641afc1befbf862edfccb2734cb61e7c036e1f1590df54c4637ee62ebfd0`  
		Last Modified: Mon, 06 May 2024 18:55:41 GMT  
		Size: 1.2 MB (1229941 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebb6da59d15c77f40b17136960f1ded0373cde8a4118bf160a7e2b7773ac0a5e`  
		Last Modified: Mon, 06 May 2024 18:55:41 GMT  
		Size: 20.5 KB (20507 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; arm variant v6

```console
$ docker pull nginx@sha256:34f3453553d07aacc354b3d9117e5ef64dd84503eeb7bf7613c00d9a73b6e069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd548deebbdf5c36208a8a0c66657a02e6ac63f60a30287a5cba74391bfee2ea`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/73d6839714a2.tar.gz                 && PKGOSSCHECKSUM=\"95d513d058493d60cba5a6bb328dc3c3e75ea115cf248a64bd921159e11c6fc87d33c7f058562c584fe440a219b931d53fd66bd4c596244b54287b62979834db *73d6839714a2.tar.gz\"                 && if [ \"\$(openssl sha512 -r 73d6839714a2.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 73d6839714a2.tar.gz                 && cd pkg-oss-73d6839714a2                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/73d6839714a2.tar.gz                 && PKGOSSCHECKSUM=\"95d513d058493d60cba5a6bb328dc3c3e75ea115cf248a64bd921159e11c6fc87d33c7f058562c584fe440a219b931d53fd66bd4c596244b54287b62979834db *73d6839714a2.tar.gz\"                 && if [ \"\$(openssl sha512 -r 73d6839714a2.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 73d6839714a2.tar.gz                 && cd pkg-oss-73d6839714a2                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a66ecc0be0a74f2d8f6a33b5ae07af0349039cb5df4fea6f2f48b735676415`  
		Last Modified: Mon, 06 May 2024 18:00:21 GMT  
		Size: 3.8 MB (3801206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23e20ba6e6fe7b75a3c433ba84a247d994ab54490d2933dad4f2694d20f6cb21`  
		Last Modified: Mon, 06 May 2024 18:00:21 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b5f20fca4236ca76f09fb80021dd6e0654a0c24fe1c21deb605120e08c9f78`  
		Last Modified: Mon, 06 May 2024 18:00:21 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ff6a933ecd54cb2cbee174187f0c6e0a8631c2c3df8048fa1ef8692ab97aaa5`  
		Last Modified: Mon, 06 May 2024 18:00:22 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d73bbe502bd338cabb6eb074691e88f2b4a4fbe550b055c17b6cf3180c1fee80`  
		Last Modified: Mon, 06 May 2024 18:00:22 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0ffb8be1d9146fc4bb0620cf709748c778bb9e6ef900493378f03c8f1223a74`  
		Last Modified: Mon, 06 May 2024 18:00:23 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d5c9878cb2cd8a6b234a4df21ecc886a6601e0962894550c8a7b2a62644a0e2`  
		Last Modified: Mon, 06 May 2024 19:06:40 GMT  
		Size: 11.0 MB (10984814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:4bdb937bb0e8164c9d0148c56ba2daef10e775f89203e748e4ab9ea1f3b925a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 KB (20380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432e28e48c61b91db3a05367cbd4d09908091dea50526eaeead16ddac7c2eac8`

```dockerfile
```

-	Layers:
	-	`sha256:f83c9857da039c3d89aef8db6629e20f9f5ae5ef500b6cc9a079747b08b6ee70`  
		Last Modified: Mon, 06 May 2024 19:06:40 GMT  
		Size: 20.4 KB (20380 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; arm variant v7

```console
$ docker pull nginx@sha256:19148fa7fbab19c0002402fd23adfc1ab4a1f3041f5b9b8a02c5c62858f1a012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17368061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc2ae1e1df17dcfdeba9151a9a1d1c39d0673c0379ba357d67e65adde7e96a8c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 21:35:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 21:35:33 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf02467fad3468c99d6c553f7b0c6b0af9c44ca2e7cac3d7097f8f822f359e1`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 3.5 MB (3512920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f2cc87ddbf7a232207e3bf45ac9d169dec50fa16ea3d3b65c104c610d49c4`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b227bb717a95e2bccd3c15c8b21fee8aca7cd6c4d92cec52add755643ee692`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693ba1e2ad342ea823fc614668a786c150c22af88d3c95e6fcc93e3fd109a416`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c514996771d85afc4209ad07d64b250abbbe2e47091008f3c3773e8e6f327`  
		Last Modified: Wed, 24 Apr 2024 01:30:57 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a85c080e146e6a089a17992d285560081f469a8cb27723f2cdbb70ef837fd39`  
		Last Modified: Wed, 24 Apr 2024 01:30:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd7576aff63658afc8b87bf55f4bc1ae532aeb0a79e945d8e00c072eb396519`  
		Last Modified: Wed, 24 Apr 2024 02:11:50 GMT  
		Size: 10.9 MB (10931652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:7e93e91bd25cc7c71659f4d634acfac85c663fac1554ef05051d261a90ee1e02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1253409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09db04716e50a02c506d56cf2a7f6dde253cd1e043c7376fd9701f6ca3316069`

```dockerfile
```

-	Layers:
	-	`sha256:4e98b33a5d7a5d8e7bb67e1e9fda8fa1fc32150e6792ddbadadccff1f7911784`  
		Last Modified: Wed, 24 Apr 2024 02:11:49 GMT  
		Size: 1.2 MB (1232571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c74516fb3910b849c1837049cac2a25033ad2a8e89c3886f0815de7e315549d2`  
		Last Modified: Wed, 24 Apr 2024 02:11:49 GMT  
		Size: 20.8 KB (20838 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:390d534999cb8e9c530b8eed66f19682d7c0377d743a92d2ebfa5ffcbc8f8e7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20171211 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fea7fc62e3a814498873aaa626553fe729f4a1931ea341cdced149c7151dea2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 21:35:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 21:35:33 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cb0812d62a99e5f18a0e22fe1370ed73dd3fbd490199715ee9f703a2dc10d76`  
		Last Modified: Wed, 24 Apr 2024 02:23:04 GMT  
		Size: 3.9 MB (3903505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddc9a9110b6c8755bfb99683ab554bbf78bcc47d30923607d432ebbe800a5c9c`  
		Last Modified: Wed, 24 Apr 2024 02:23:04 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9321fb387d23ee85264f1857036daa91a56c9f3d7c56f754994caf40c23427f0`  
		Last Modified: Wed, 24 Apr 2024 02:23:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fcc7bf14b1236506a8a135762d162558179d6f1728284d3abaa35da3e684d15`  
		Last Modified: Wed, 24 Apr 2024 02:23:04 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c87ab2be7114681a4596fee8b8ceee779e347e2690c12f424a39d6607bad58`  
		Last Modified: Wed, 24 Apr 2024 02:23:05 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:396a20b72eb6974d9bfdf97bbf34f8d201fb438181a20b6dd9857c39de40d9ab`  
		Last Modified: Wed, 24 Apr 2024 02:23:05 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b93fcabe93e524322affe85251b88bef575ea7f0cdc56b964f8fba1bd452d7a6`  
		Last Modified: Wed, 24 Apr 2024 03:16:19 GMT  
		Size: 12.9 MB (12915401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:2b51fc9b97bc55884ed4051bac674aa117e7008de306d0561c3f45fe5882ab55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1250723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4029c3f6d66d86514b11207148d26ae81c69c308733a44d369e48b57df38cb3b`

```dockerfile
```

-	Layers:
	-	`sha256:5e337d1302fdad221d22faabe92f8159816f8dbe29fe6a44e129ac730b967ed5`  
		Last Modified: Wed, 24 Apr 2024 03:16:18 GMT  
		Size: 1.2 MB (1229956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bd838513ff0bae07e40717ffaaf91d23ad09e1439ab5494b41196bf66a4e1a1`  
		Last Modified: Wed, 24 Apr 2024 03:16:18 GMT  
		Size: 20.8 KB (20767 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; 386

```console
$ docker pull nginx@sha256:9e66c581d5848c3ccccd9e960e43cc60f8d9712cc393c545739fdb48632fcc68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19255195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ef395cab6d34adc41ee4ca345762d15d731fb84960a2e6acd54b767aa1327f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.26.0
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/73d6839714a2.tar.gz                 && PKGOSSCHECKSUM=\"95d513d058493d60cba5a6bb328dc3c3e75ea115cf248a64bd921159e11c6fc87d33c7f058562c584fe440a219b931d53fd66bd4c596244b54287b62979834db *73d6839714a2.tar.gz\"                 && if [ \"\$(openssl sha512 -r 73d6839714a2.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 73d6839714a2.tar.gz                 && cd pkg-oss-73d6839714a2                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_VERSION=0.8.4
# Fri, 03 May 2024 19:49:21 GMT
ENV NJS_RELEASE=2
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/73d6839714a2.tar.gz                 && PKGOSSCHECKSUM=\"95d513d058493d60cba5a6bb328dc3c3e75ea115cf248a64bd921159e11c6fc87d33c7f058562c584fe440a219b931d53fd66bd4c596244b54287b62979834db *73d6839714a2.tar.gz\"                 && if [ \"\$(openssl sha512 -r 73d6839714a2.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 73d6839714a2.tar.gz                 && cd pkg-oss-73d6839714a2                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9aa7ab93543be4997d8e5cacc2d47e1de4b8d77965ca5c245e6078d24db8626`  
		Last Modified: Mon, 06 May 2024 17:59:22 GMT  
		Size: 4.0 MB (4013705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:662a3491e13b430d0455fd6935c0969a795ca444d1c1645377fa5bec5d025083`  
		Last Modified: Mon, 06 May 2024 17:59:20 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8325fabeb41b9d441093932bf0087c2120480ba718e88535f99754ebd0dec1c7`  
		Last Modified: Mon, 06 May 2024 17:59:20 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c48d5e979fbe711d97d3da7b135cc8834fafa46d7221d9c14aaff7925c991b`  
		Last Modified: Mon, 06 May 2024 17:59:21 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51472c36cca973931ffc1bc90a2dc64abe6ca885d1eddfc9e9d00f748dedb361`  
		Last Modified: Mon, 06 May 2024 17:59:21 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b613b6b436417fc728ef352ce90bb1ef1344f0b6acf3d9adb09129df0d39b9`  
		Last Modified: Mon, 06 May 2024 17:59:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc1a18cef091df300b782bfc597a7f0df0101e71c958c8add648347d8df2795`  
		Last Modified: Mon, 06 May 2024 18:59:42 GMT  
		Size: 12.0 MB (11992816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:085835e8466540fa98add845fc9feef5d6733cc6e59d277888174b5c53123530
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1250371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8e7419e2f6802043beac517950f3a159f6b8922892c1854451002b699fe705a`

```dockerfile
```

-	Layers:
	-	`sha256:934fbefe07b50e264f427c603d9a66c8f91d2d7adafbf00c2355c2c0c0f049ca`  
		Last Modified: Mon, 06 May 2024 18:59:41 GMT  
		Size: 1.2 MB (1229906 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f9d45ea6d7bce94c5e499b32d72707d8db9b72045e3d7d9b2a2d6f498e7c7fc`  
		Last Modified: Mon, 06 May 2024 18:59:41 GMT  
		Size: 20.5 KB (20465 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; ppc64le

```console
$ docker pull nginx@sha256:454ed99ebd8d6ee1e95889de1e7bed7884d8c6b6dc7cbea62c6f26b942e0c0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20477579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d84f86b77f5da61e62a5474186d3beea9ff3cb55747dd9eda229d67bd41e64c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 21:35:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 21:35:33 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5842680d7bb2e7e5a243413e13113582352e3da959b9ceb824bba7d327ef99a7`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 4.0 MB (4044107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ff777fc13b28a36f88ef42d61af715184659340e80729633e0c212758a1621`  
		Last Modified: Wed, 24 Apr 2024 01:47:39 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f5f7179c98fc0e8f482a5b9a085ad8967d9691077b70ea075d3ae1511683a2`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2828c9c8f9b99633201aa78a8c68ee15a739e80b97a77544d5341296aad317`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe46d9fe812b55f7ed6e7ada3aeb08825a9609ededd03eafbe3392f8a8f658`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f49548c9348f9487c118e382ebd22cce9a995c68c74c529a1e3761f2eae3abd`  
		Last Modified: Wed, 24 Apr 2024 01:47:41 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dde1617f513e58120bcd834ef759f93c19a0a11e1899e30dd17fba414a7721ee`  
		Last Modified: Wed, 24 Apr 2024 03:09:23 GMT  
		Size: 13.1 MB (13070536 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:5893722456d949cb5d25df0d9c85a35dfa5516c75a79357a7f9838eacf7881a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1248837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36d19cf31f4350bfcea13ac5bb621aaf1fe02542bbd5abc3d3cea6ec125c2542`

```dockerfile
```

-	Layers:
	-	`sha256:31ce87cd5a6df685a9f1e25f865f6930950c50d0c2d0aa45b52fd16599cbd17d`  
		Last Modified: Wed, 24 Apr 2024 03:09:23 GMT  
		Size: 1.2 MB (1228033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e8d96072f0c0af7ce645bcd4cb5d54c05c7c25912c7fe9670e1be7c4aacdf71`  
		Last Modified: Wed, 24 Apr 2024 03:09:22 GMT  
		Size: 20.8 KB (20804 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine` - linux; s390x

```console
$ docker pull nginx@sha256:5804e11061eb750f4f7fb35703ccf707ede48640a6fdfe43d0f69055e817b03a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20286095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23fbd034aab97bd63b50423ebfb8cf7c60eb3c8aec7bfce29d49718a5d0b2fe0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 21:35:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 21:35:33 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d94a7e88836152f6e5ef2857a7c6d914ba17974891424e7d1ca48e44618af3`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 4.0 MB (3959358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a951cb40a3a3a8eb67555bc9127380b5d6d8649f71be69b1356340fdf0f7d`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81834bfd250003c18f8a15c0799a1c354a4dcf4018f23ba960a8217ad428cf7a`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce4a4c046e97fb7083c5938ab708890488eca1189a981f32c5951a30953382`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6890302afab99fa6316e89cc4e8fc2a7841e7a617b656c6c2989bb67179f94`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8135d2eb47d1611822918bbdf0683a72705af33764ddb656b10909ee54bcfcb6`  
		Last Modified: Wed, 24 Apr 2024 02:09:12 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52c25fdaedae4cd72ab3621e23aaf4277cd6c22a2628d8eed00f83901d20b518`  
		Last Modified: Wed, 24 Apr 2024 03:11:48 GMT  
		Size: 13.1 MB (13079520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:513957aa270c62b6b2898095f9dfcff97efe2ff53417c5da81118cb6d0897b06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.2 MB (1248735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1306f3bc43780ca4567f7fc3cd9c43bc1a4efa859f705aa3a8a29979e513e5bd`

```dockerfile
```

-	Layers:
	-	`sha256:bffcae215e0ac7ce40b700ee87f8c5cb39c554f45083eb5beeca413d26e57bfb`  
		Last Modified: Wed, 24 Apr 2024 03:11:48 GMT  
		Size: 1.2 MB (1227987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d35beec0cc800e552505e4ac8597aaf85717b77b4893dfc3e98a6aee49119e22`  
		Last Modified: Wed, 24 Apr 2024 03:11:47 GMT  
		Size: 20.7 KB (20748 bytes)  
		MIME: application/vnd.in-toto+json
