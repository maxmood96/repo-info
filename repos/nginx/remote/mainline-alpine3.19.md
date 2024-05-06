## `nginx:mainline-alpine3.19`

```console
$ docker pull nginx@sha256:fcae72aeb84043f1ecf860b0c5c31c8a8465b5c503e123c9c94b3fd55b82376f
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

### `nginx:mainline-alpine3.19` - linux; amd64

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

### `nginx:mainline-alpine3.19` - unknown; unknown

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

### `nginx:mainline-alpine3.19` - linux; arm variant v6

```console
$ docker pull nginx@sha256:eb7ad97a0891637093894d20a941117cf55a16cbe0bed41187fb0be17e2cc93d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17955998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b2b1654b577d3dedc273a27e6a937e7bd62f62b4411209eb0fcfcb99a641f78`
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
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4c710658b05998808bdad148bbff2d4ffaf94b911fe0a02c853faeb203da254`  
		Last Modified: Mon, 06 May 2024 17:59:13 GMT  
		Size: 3.8 MB (3801207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4da322acc53420c562d4cbe41e4c1c747d67128d5a4f91df2f092887880c7f3`  
		Last Modified: Mon, 06 May 2024 17:59:13 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c75232d8d77d0c79cb14d2f1161fded162a78f24047fa593eb535bee353908bb`  
		Last Modified: Mon, 06 May 2024 17:59:13 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b576bda25886614caa2d55c99888bf7ddfffa6d1015f8f53560e29722582259`  
		Last Modified: Mon, 06 May 2024 17:59:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d24f672e0bfd148b422bff3b395347ffe28cc41acef81b4a62b59a573b7ed434`  
		Last Modified: Mon, 06 May 2024 17:59:14 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a54986d7c96eb59eae832459f9792412e699ba0816be8feedd4a93590cb48a89`  
		Last Modified: Mon, 06 May 2024 17:59:14 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dec77ef04cfc90b2c49671608ddc5cf796804698c76590e4ea04524d95c04a8`  
		Last Modified: Mon, 06 May 2024 19:03:22 GMT  
		Size: 11.0 MB (10984813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:d86f18cd2ede5911adf2781d1a68958b6f5d6fccb150696fe1abce2b573668d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07afc506ce02b328bdd644fee2fcd7f9f4867f11ba06379d699f8a758f772ddf`

```dockerfile
```

-	Layers:
	-	`sha256:7e8834ba2ddf20510a5347773f769c0b9cc49d8dd04ab8a9b662cb9a5e3c11f1`  
		Last Modified: Mon, 06 May 2024 19:03:21 GMT  
		Size: 21.7 KB (21653 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.19` - linux; arm variant v7

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

### `nginx:mainline-alpine3.19` - unknown; unknown

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

### `nginx:mainline-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:1f37baf7373d386ee9de0437325ae3e0202a3959803fd79144fa0bb27e2b2801
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20171257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e664fb1e82890e5cf53c130a021c0333d897bad1f2406eac7edb29cd41df6b10`
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
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=2
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71b5d20449d6c1deaa6ae50e1312bea509ffae6dea2e84806a8f266b46eec271`  
		Last Modified: Wed, 24 Apr 2024 02:21:59 GMT  
		Size: 3.9 MB (3903515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d4387dd11cc0dc7fbcba57b7e80136983a6b28e8b30b5aad71cf9cf0937646`  
		Last Modified: Wed, 24 Apr 2024 02:21:59 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a678d724fd1e7b9fde542fd38982db908f78a6c8ab628a4397056fd4536d3d31`  
		Last Modified: Wed, 24 Apr 2024 02:21:59 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4515b1dd221688d1202be5e7c173e85a00c14a3caf933daf1fcd32b482202f5f`  
		Last Modified: Wed, 24 Apr 2024 02:21:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7637b7f17b43f692d2b6649359b2d4ffb0748ccd4e9725d930bf1ebd85b1994e`  
		Last Modified: Wed, 24 Apr 2024 02:22:00 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a93a75238318615135c222e3ea2764a9663d37f7f2e275bfb76e9f1baf1038b3`  
		Last Modified: Wed, 24 Apr 2024 02:22:00 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97fe46bdacf05b7e6a366f23aaa4a4a5889db20f54534a3d41932a761881a5eb`  
		Last Modified: Wed, 24 Apr 2024 03:15:56 GMT  
		Size: 12.9 MB (12915439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:070d2a04985867bb429e7ce6ec6e276146aac9fbc34adf672fb065e1a788883a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1252974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0bf975c8b474a514d4e11f1dce5c923eba42292e198ff72f3281a08970b6250`

```dockerfile
```

-	Layers:
	-	`sha256:6d008e0f0913c506afa01c08c3b6c28746e73e5b05942e2e4b1a498beb03e39a`  
		Last Modified: Wed, 24 Apr 2024 03:15:55 GMT  
		Size: 1.2 MB (1231180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc1e690896ec6de9c8253753d374a1b0c56619601b1000866af23a1c156caa81`  
		Last Modified: Wed, 24 Apr 2024 03:15:55 GMT  
		Size: 21.8 KB (21794 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.19` - linux; 386

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

### `nginx:mainline-alpine3.19` - unknown; unknown

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

### `nginx:mainline-alpine3.19` - linux; ppc64le

```console
$ docker pull nginx@sha256:17aff5988d1e3c2417e754b5553fbc06b0f0165451ef2584d04bd79899139de4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20477488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6fe4b91fc80c97a8452a2835456b2156f57be9862fd036bf04965e83c77a963`
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
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=2
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e19be3f9fc7558832c114fcb8f0d0150948f2823f5cb35ecd33cbe5319bca45`  
		Last Modified: Wed, 24 Apr 2024 01:33:52 GMT  
		Size: 4.0 MB (4044034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66bc88e654f4f04cde664d8d6689f26b6dd0e974a57ab38a115d404f9d3ded86`  
		Last Modified: Wed, 24 Apr 2024 01:33:52 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1659af7c3423b2c4b3a77c1fcf8225857fd3e2c0f03fdab65fa94277f06d9664`  
		Last Modified: Wed, 24 Apr 2024 01:33:52 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef15f617be151acb06ff24206721e6b4aeedcaf715d632fcf32b97f874c7627`  
		Last Modified: Wed, 24 Apr 2024 01:33:52 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f856eafe0363466338530bd27bd13061d094e47cb6b2a22d1fed15c39a100d1`  
		Last Modified: Wed, 24 Apr 2024 01:33:53 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db0de99fded0d707764f5b8ca27395c558f42348f608226bc5391dd06be7e26`  
		Last Modified: Wed, 24 Apr 2024 01:33:53 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7ec1b36a1cad93e0a58e8836f831ac276d12c6ff1aa38159f08a62b9273eb80`  
		Last Modified: Wed, 24 Apr 2024 02:13:27 GMT  
		Size: 13.1 MB (13070514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:91b5da153ddd76e7b6f8c596811418fc05b049aaa160a0187ee98f9948f2cf89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1251119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32a80a0dbc4a2d3a8caefc6e9f5205e3c722b65194e155457f1a0d87c9dd3e01`

```dockerfile
```

-	Layers:
	-	`sha256:6d52381293aa75a33903f7c9b24343f5bbc28a93db01583bde03304c906747ec`  
		Last Modified: Wed, 24 Apr 2024 02:13:26 GMT  
		Size: 1.2 MB (1229273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74102916492bb972103aa7ec48d9e014399be094f5872b91824b6b968dbcf50d`  
		Last Modified: Wed, 24 Apr 2024 02:13:25 GMT  
		Size: 21.8 KB (21846 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.19` - linux; s390x

```console
$ docker pull nginx@sha256:5ac7db20bc10c0e86dadc1c57d8f93e250698610087bdfed9054d2b16b379f64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20285920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:711725ff9e51d92db1103845220c1ea133c6fadc3a11e6038834a081d7434a74`
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
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
ENV NJS_RELEASE=2
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a835c8447315f355527bd300e97b8292aa87f7b0f0c7f8617522bdfa348ef432`  
		Last Modified: Wed, 24 Apr 2024 01:48:33 GMT  
		Size: 4.0 MB (3959378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a291f587038e560ba7fa07e9c0c1fa628de707052183eac984b1d7936ced90ce`  
		Last Modified: Wed, 24 Apr 2024 01:48:32 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c08f91fcdd4f2327edd7eacd473cce166bbce55cf23c466791d779683d85917`  
		Last Modified: Wed, 24 Apr 2024 01:48:32 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60c79d1fd695e9d5e858b8eb344ad29b010d4971009685ec38412e6603571c4`  
		Last Modified: Wed, 24 Apr 2024 01:48:33 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d0f188d9cb7e2409ef2450dd83c26be1e574eec73c157ebb7087d1e2ba153d2`  
		Last Modified: Wed, 24 Apr 2024 01:48:33 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44010dc87733fcd716f28840bbc98faa4099feaba1c2d9173722c7cc140355bd`  
		Last Modified: Wed, 24 Apr 2024 01:48:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:719d07fbba0ab461ab59a2e5f7fc8cf2d274c93fb43f2c8586d41a266908f054`  
		Last Modified: Wed, 24 Apr 2024 03:08:56 GMT  
		Size: 13.1 MB (13079321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.19` - unknown; unknown

```console
$ docker pull nginx@sha256:56817ea1f04f76d3068754aeeb8f55518b6ea683bd62f8d6f056bdad5283cfb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1250969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8a6bc194a942821b88acfafd09a5b3c7f2d6e278f5b9af7fc8a4eadcaebe9ff`

```dockerfile
```

-	Layers:
	-	`sha256:73fc3d95ad7bd4b67daeef5e764ee0435ec088fd386aae9725465d90c3ddbda7`  
		Last Modified: Wed, 24 Apr 2024 03:08:56 GMT  
		Size: 1.2 MB (1229203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:192560e5ecaa576de7b1d5dbfc37a778b2353bb07346a50cc9eedd41123558df`  
		Last Modified: Wed, 24 Apr 2024 03:08:56 GMT  
		Size: 21.8 KB (21766 bytes)  
		MIME: application/vnd.in-toto+json
