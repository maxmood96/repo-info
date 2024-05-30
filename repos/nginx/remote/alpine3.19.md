## `nginx:alpine3.19`

```console
$ docker pull nginx@sha256:2a033afa29d4105f35f2ba678d11a216d0fd86b2e523ce709b241259274cb77d
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

### `nginx:alpine3.19` - linux; amd64

```console
$ docker pull nginx@sha256:721fa00bc549df26b3e67cc558ff176112d4ba69847537766f3c28e171d180e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20438864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:501d84f5d06487ff81e506134dc922ed4fd2080d5521eb5b6ee4054fa17d15c4`
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
ENV NGINX_VERSION=1.25.5
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=3
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc21a1d387f514f53589abea6d67cd6b329dfd3c9059bc96a552af3b3c97b413`  
		Last Modified: Mon, 06 May 2024 17:57:39 GMT  
		Size: 4.0 MB (3985350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6ef242c157026935bf8a69e6cf19f8f6635e44507c813daf0cc644f2e22396b`  
		Last Modified: Mon, 06 May 2024 17:57:39 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13fcfbc94648785b918ecc1af675ac5187cdfc30f4fdaf9afa8bd2e9dedf548b`  
		Last Modified: Mon, 06 May 2024 17:57:39 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bca490e609acaaf54ca73363442d31a31fd136a47a20a12370cf2025f0a10b`  
		Last Modified: Mon, 06 May 2024 17:57:39 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5406ed7b06d9a94b5bd15843d2a1c7e38796a3ec5dc7f40f16f70cc1d045f453`  
		Last Modified: Mon, 06 May 2024 17:57:40 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a3742a9529dc5c00974dfcf5e465be9f1606ff8a1911527b3928cf86ad57465`  
		Last Modified: Mon, 06 May 2024 17:57:40 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0c16747d2c6b6c26c064652afcb964c15f1b1e596ec052b2aa19b83948ae27`  
		Last Modified: Mon, 06 May 2024 18:55:45 GMT  
		Size: 13.0 MB (13040202 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:df1639f64633b8ce4b549aaa27e5bed796a25240971e4798236662a090c73130
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1252905 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a45708c4b80ac0b255bcd444bae0f07db8f1e144ddc364be090c8887b3bbde7`

```dockerfile
```

-	Layers:
	-	`sha256:30d1be61be1407327b8f2933eac618100000a7b22d097560c2e02bf78c9897c7`  
		Last Modified: Mon, 06 May 2024 18:55:44 GMT  
		Size: 1.2 MB (1231157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc44f5562637baee319fce1cba87ed18f09b4fe2c588f715e60e4625a56fbd5d`  
		Last Modified: Mon, 06 May 2024 18:55:45 GMT  
		Size: 21.7 KB (21748 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.19` - linux; arm variant v6

```console
$ docker pull nginx@sha256:0608b4ccda75be0ba50f3cf28998b60d31fe0ad147cd834acb1451ba0da84c8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17960124 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bdede6a0ada9253049e985bb5bf165639dfc61113cf45f6e4eefe61d156f1d3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"cd3333f4dfa4a873f6df73dfe24e047adc092d779aefb46577b6307ff0d0125543508694a80158b2bfc891167ad763b0d08287829df9924d4c22f50d063e76c0 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_VERSION=0.8.4
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_RELEASE=2
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"cd3333f4dfa4a873f6df73dfe24e047adc092d779aefb46577b6307ff0d0125543508694a80158b2bfc891167ad763b0d08287829df9924d4c22f50d063e76c0 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ef88ad30fd0027ecdf5a07da554daea1099b6ccbb4911593dc429cc2b1eb6`  
		Last Modified: Thu, 30 May 2024 15:57:31 GMT  
		Size: 3.8 MB (3805253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30589f30348bcd6c5e77d3fedb7f3906517dd5e4231d90776c0f837b387acfea`  
		Last Modified: Thu, 30 May 2024 15:57:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd715eed8aa3a129ace8df63e69b7bdcc0544ed3819f79ef4c930be692fdd4f0`  
		Last Modified: Thu, 30 May 2024 15:57:31 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ea2a6dac2b2eb4bb8c5d9b798a2809a299d9180bc06587cd17e2e03e2b80d`  
		Last Modified: Thu, 30 May 2024 15:57:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d20b1665bc2a56011bc9d229ed19e110d0fad9f48c25b19599ab9788efac38`  
		Last Modified: Thu, 30 May 2024 15:57:31 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac79ab8904f186419342b9ec6cb03645472c1e4040d815c831a986c7686bfe87`  
		Last Modified: Thu, 30 May 2024 15:57:31 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f3284fbae87a1b1e4db8fa529d8279a1e68146b2da6da25497da0c43b1613a0`  
		Last Modified: Thu, 30 May 2024 16:57:20 GMT  
		Size: 11.0 MB (10984873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:3ce57bf95a2c77413572c51b8aaa2f280e0ac38e0c4bb329f73ded75e1e22d3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 KB (20797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab2073bb0e7c248fa60be25800809afc500c2220be5d68a929a1f3316cfa29a`

```dockerfile
```

-	Layers:
	-	`sha256:e3dd56e5dd5031c1a0ccecf4bc0d717124fe41115a54d68b6439b003daa23e12`  
		Last Modified: Thu, 30 May 2024 16:57:19 GMT  
		Size: 20.8 KB (20797 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.19` - linux; arm variant v7

```console
$ docker pull nginx@sha256:256709e9edfc22eafe9415b386f24dca0c8f8945063825306f042b777b67fea6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17368016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1de3cdd3c7f5236d1032d04b168dd87f40918cfef4983239adf6fb719eb4fd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.25.5
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=3
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83a58c3b3168b3bbfe556b5f0cc92906fa75538e0a4b41896ca36bb61d61fb0a`  
		Last Modified: Mon, 06 May 2024 18:49:16 GMT  
		Size: 3.5 MB (3512930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffb11eb5cbffc36f47dd68287139902e4ac55b2b182c214e62c4bb184a54f6ed`  
		Last Modified: Mon, 06 May 2024 18:49:15 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b53e2922332a231f40129bcd826c3693952d749253fef7a31172736f9f28cba3`  
		Last Modified: Mon, 06 May 2024 18:49:17 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba5efd047dbb3c1025c6a6f6c8e3cc2817b90d3f6b967ed0db0d988297bbd65b`  
		Last Modified: Mon, 06 May 2024 18:49:16 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a54919c0f3cb9e3dcff1524c93cd4633d291101af52f3fb32eaa1ff3fdf7c4d`  
		Last Modified: Mon, 06 May 2024 18:49:16 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a1c13f9c886475f98864584b864a99ede88ff04366e1e09c173483bb46e5c0`  
		Last Modified: Mon, 06 May 2024 18:49:17 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bffb6ae7aa5ca2f34e1ce66955b8130c0313af4d8bc2d15d3b5d0cfc263700e`  
		Last Modified: Mon, 06 May 2024 19:24:30 GMT  
		Size: 10.9 MB (10931596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:cfa40819a70c151297d630ccbc2aae3d4d38d9092bdd90009ddbe939e005e285
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1255708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15639803bbbf909f18afc0636c8320d23b0d5a7e2178bfc1acc3675d7ecb5a9`

```dockerfile
```

-	Layers:
	-	`sha256:bcf14b54a3d120079279125404e10976f138505d94773d78b55edf53e2fc134a`  
		Last Modified: Mon, 06 May 2024 19:24:29 GMT  
		Size: 1.2 MB (1233819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3f2b2c6409fb0289e70a210ea0cd32aa45bed359cf45bd36d8ff2e32608c51c4`  
		Last Modified: Mon, 06 May 2024 19:24:29 GMT  
		Size: 21.9 KB (21889 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:05325b3a32db871dc396a859d9a9609d75f50d2f7ad12194f9f3a550111bdcaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20171279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6767b714bf1ecd2cdab75b590f2c572ac33743c7786ef5d619f7b088dbe0bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.25.5
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=3
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf9db5a05cbf61e62d46b1225986f3238390e770aedf7c3633b0f4984df6a6b`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 3.9 MB (3903507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83296a673ce8848db1a03260b4104984c299b3619a73842eeecb887e6ebd1c0`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3127eb6227853129ee22d81700ccf48bcdcb17929680fc9f01ac3c7bc6dbd`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166b80e00f74c3a053c98236bd987af4ee91e23276257bf52858ebc900d55bb3`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e691fb2cc710f857dcd9016d4854cea790a28508e33bf2ef928f61ae6c4d6`  
		Last Modified: Mon, 06 May 2024 21:13:14 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff282c446606ae80b6c7812c9248a7b9d56f86b18c0b9b068ba821517cdb66`  
		Last Modified: Mon, 06 May 2024 21:13:14 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f6b4e3940df0e5a4b975a6943afdcd034a2a0e2404258436cc76fd145d04d0c`  
		Last Modified: Mon, 06 May 2024 23:45:28 GMT  
		Size: 12.9 MB (12915469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:44f5007dfda048eb4a61e7c852b8b804206dd1172896a1498a75d86b05694947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1252974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45f9d8cd99bb88e9b9e659ea51f4a2b6bc15c49fc03c31ea0dec4ad863d78c3`

```dockerfile
```

-	Layers:
	-	`sha256:beae44954c403e46275b0eb95c70a9e03c820b264dc2e4d340bd1c6bf827822e`  
		Last Modified: Mon, 06 May 2024 23:45:27 GMT  
		Size: 1.2 MB (1231180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be49f1d24740d37adfca5dc096ff20ee2bea644f5fe16b3e4467e73f5baf205c`  
		Last Modified: Mon, 06 May 2024 23:45:26 GMT  
		Size: 21.8 KB (21794 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.19` - linux; 386

```console
$ docker pull nginx@sha256:69fcc4e1cdddc63735fdd0ff4aea1d467120238a2e8d0767c596517664eac19e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19255140 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d942fdd730a7058a7d67f677141721957f4d104824bfba81a705cfbdc3881633`
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
ENV NGINX_VERSION=1.25.5
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=3
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:093b20a2f2c2b4ff878c60882c4d43c3084d4c5e951e2480a9cc01bb1cf52670`  
		Last Modified: Mon, 06 May 2024 17:59:18 GMT  
		Size: 4.0 MB (4013709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73a2f02e459b7f1eb62c38b178f5623a68a3f04445778e9f79dc34f61cc0a49e`  
		Last Modified: Mon, 06 May 2024 17:58:02 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea9afe72057936b64c5a37b539b21e2b129eb9b55e891fa30e8c5a35f2249c4`  
		Last Modified: Mon, 06 May 2024 17:59:17 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e7ba4751b51458f836c5b518a13afe826a0a47b3416021979bc4ebf4da55789`  
		Last Modified: Mon, 06 May 2024 17:59:18 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2673fa8cdab9a4348d4f2eccedc0c8433af8b98a1477942ca2d2eb2e457311d`  
		Last Modified: Mon, 06 May 2024 17:59:18 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13cc05656d385836b61fdaee5dc1353a951e1c38010cd97023d961294cb37b5f`  
		Last Modified: Mon, 06 May 2024 17:59:18 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27007b08c2599a86cb1bbc6cb9122d60cc4e64ae9a1a03df6323c14761b31869`  
		Last Modified: Mon, 06 May 2024 18:59:35 GMT  
		Size: 12.0 MB (11992758 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:960ce3021151ea67b189243e0b4fae0828395f8dd7649ca51d28d9e193eb9fdc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1252788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59901dc61dab8175104b38f202b8002a18b6df50c3b8648aff73807a0a4da27d`

```dockerfile
```

-	Layers:
	-	`sha256:183d6d4a3b140195dec27c8037ae5c5d69ec8ff14465266cdaa5afe646c3e621`  
		Last Modified: Mon, 06 May 2024 18:59:35 GMT  
		Size: 1.2 MB (1231102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87767aa52fe820ee8eeec508cdd54050b341db8c74c7ecebed89ebd6c53c4e6f`  
		Last Modified: Mon, 06 May 2024 18:59:34 GMT  
		Size: 21.7 KB (21686 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.19` - linux; ppc64le

```console
$ docker pull nginx@sha256:080f9314d8ea87949621475e1da76267d311928f93a87626a7c2c96287bbee6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20477476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb59af63b308022866eeb2e692ae01c4abe2d19e757a625c5d946d30133a077`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.25.5
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=3
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b07d3640c34ed6ecd59af50e90ea29a1804af51c13337da22e12cd5b3dbbbdc`  
		Last Modified: Mon, 06 May 2024 18:19:28 GMT  
		Size: 4.0 MB (4044033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95139aad18dbbd7b9348ba9fc253c9ecbd31fe364815fe28c9f6ace6a837bbd2`  
		Last Modified: Mon, 06 May 2024 18:19:27 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9883eafd2ec7d8f51fb6e20bc5dc9a0f90cce4686ca855c8d6d00721a3b30fdf`  
		Last Modified: Mon, 06 May 2024 18:19:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0476d3f9d7e6fbef7a0a3fcd4883f9d6c6aa9ac13295c8a06aa71e18cf225c21`  
		Last Modified: Mon, 06 May 2024 18:19:27 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c1acc852864f53505f19b2e2ba1db3c2a7aff3c5dd5f0c269038177a7812685`  
		Last Modified: Mon, 06 May 2024 18:19:28 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f391423626bae742779a90ecff90875ceb6485fe667fba151fa2932c83335a7d`  
		Last Modified: Mon, 06 May 2024 18:19:28 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8bac4720261e882013ec8a850b0b0abd5b650c85f35e3b01e1ca87b2e6ca421`  
		Last Modified: Mon, 06 May 2024 19:52:20 GMT  
		Size: 13.1 MB (13070498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:7a2c459b4cca4fc1c871b3e1f0d6d43339801fbce42f23bcf90a641d20a2e503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1251119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:373f47202798a6fb95c156020c4fb3699396677d43a7977505b7edc8a8804092`

```dockerfile
```

-	Layers:
	-	`sha256:fc0b8018003af4328239e56a77616b9a4e38d350957440b8b7c8aa0b8667c725`  
		Last Modified: Mon, 06 May 2024 19:52:19 GMT  
		Size: 1.2 MB (1229273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a7cce2b3efafff31b537559fc55e0046820cb6d5e40ea8137fcebb1e568c634`  
		Last Modified: Mon, 06 May 2024 19:52:19 GMT  
		Size: 21.8 KB (21846 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.19` - linux; s390x

```console
$ docker pull nginx@sha256:9285c3161b991178a668a4e331b3958be22daa69c4321212fd7ef45300cdc62c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20286170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26ef90740fb991f07308bb9c0f23b9a8ad266e12b995d6ba574d9c31b937412f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.25.5
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=3
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2509442efccb50439ce508767abe41c4d9c7aa806664d95e25e07f1e89d88e5e`  
		Last Modified: Mon, 06 May 2024 18:14:40 GMT  
		Size: 4.0 MB (3959394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0b45da1bb1aac6d42cc0e7d105caf3243a364ce696c076f3ea960498331cef`  
		Last Modified: Mon, 06 May 2024 18:14:40 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590972e28b92f5fb5c700190105f99d027cae23eac5571a01317f0ca0111ceaa`  
		Last Modified: Mon, 06 May 2024 18:14:39 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dffff4de60e465a24f820ab768d57980203036d807bb943bbeec9889c3d4f36`  
		Last Modified: Mon, 06 May 2024 18:14:40 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac3ba7bd6d27e11c8cb8ef8e9e0ecca11b8fe69c8f2e7f5e79bfc65607a37b42`  
		Last Modified: Mon, 06 May 2024 18:14:40 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14550138999d85cd0fae289e661feacd9193edac634ab7df4840161835ab521`  
		Last Modified: Mon, 06 May 2024 18:14:41 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ca2210167a3152fe52720e17e01827ae13977ec86a5ff9ebc8d3274b6cc559`  
		Last Modified: Mon, 06 May 2024 20:21:25 GMT  
		Size: 13.1 MB (13079552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:c0a567b52f8c73f621654bca6125dcdf9953c25028707838a8c1987ca342317e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1250967 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33fbc687a686c63fa529f2970a6f8613c0a9d481d15130d5d891d7d73efdc5e0`

```dockerfile
```

-	Layers:
	-	`sha256:9583a5a9411828fa9966f0939e6963ca56987908d73afa9623041b6d0102a424`  
		Last Modified: Mon, 06 May 2024 20:21:25 GMT  
		Size: 1.2 MB (1229203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cdeb84540adb3c68126bb3666f6f64e75b23295eae942f09671a7d5f8b9d047f`  
		Last Modified: Mon, 06 May 2024 20:21:25 GMT  
		Size: 21.8 KB (21764 bytes)  
		MIME: application/vnd.in-toto+json
