## `nginx:alpine-slim`

```console
$ docker pull nginx@sha256:7c978471d4dd0e9b82314468ed7543f6bba6035f30fee57c4e12a662d5a25f53
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

### `nginx:alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:eda8e5b6782f183d80dff97daf777918528bb43bb8845684a58b22f94730632b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d065ef312e2d0ce2599a1936214f7c21f5c122541439630621eae142d3e8cbe`
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

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:a0b05e56571c060c0e45fae757908ba0eba2e1b88afd1493299e94f9634db82a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.7 KB (869714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c96d804ee963529e271cce3b4af1cb417b266bc9c025b21c2c6fde1920f2270`

```dockerfile
```

-	Layers:
	-	`sha256:47a5f874ec861a28063ad600bcbd20f40ae3205144bfecb632bdd3bf7aac093c`  
		Last Modified: Mon, 06 May 2024 17:57:39 GMT  
		Size: 839.5 KB (839468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db6a84b87970e4f98639a76001f67bd3d282d38bfc23000e55ac17cb9dda5f17`  
		Last Modified: Mon, 06 May 2024 17:57:39 GMT  
		Size: 30.2 KB (30246 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:5eff2e82bdbbcf91963d11774886532343aa3dc8aa1340892af7a97d92ddea00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01768785a325ff698c9c1005076f65bfca75d5bbcf872b5e4fd478861742decb`
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

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:f7aab654558a12cd7bcd685afcf24c198afeea7347c87a6e49f62ef550360120
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.1 KB (30145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:562c422df5c920cc8fe317ef3bd6a45e3dab9fbb797ce9577c56dbea95a80f25`

```dockerfile
```

-	Layers:
	-	`sha256:d16c8e5907cbd06c507d1205cd4f7fb398333b25aa6cadb9b72a8775611b7735`  
		Last Modified: Mon, 06 May 2024 17:59:13 GMT  
		Size: 30.1 KB (30145 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:5f8000667e533e39a29ee13975b285d2b7b9552d395a91c7a558fac59a8e5c42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9939d022355269afbcf367aa09b2bd15f67749a4c2a7981a217f2da7f6d382`
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

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c2b64bb967959b78dce2658b9c229627b480d56db4bcad9a06c16b44fbf83c94
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.8 KB (869750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76104c54ce811f24bebf3b0bd67aedda9bb517804524ac1c6d5e7e79e8f7ac05`

```dockerfile
```

-	Layers:
	-	`sha256:c5b29165ca7417226cb6ca20abf54d69b91c11406e808b2fadd3f8a69a4ff2f2`  
		Last Modified: Mon, 06 May 2024 18:49:16 GMT  
		Size: 839.6 KB (839552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:38fb0c3039d8cabd679b0b345d67312e6009bce8a1958f71b14d64a1c1e92ddd`  
		Last Modified: Mon, 06 May 2024 18:49:15 GMT  
		Size: 30.2 KB (30198 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:7878a1d9f3bdd16baa8d7b2aa2258f7440862a904ad797f8026ee201b74feb21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7255818 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:559ccf8c22a38ca5db81ab24b767f64a4ddf540d3a85ac8b1150f01a1ccc04b1`
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

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:626215f39226779d6a97b2b25e70f848c7a14aae6f0466bd2d0e3297c0062470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.6 KB (869593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f528ab068349070e7e74213361322d22e9e947e33fb78da84ca8ade4becd7b78`

```dockerfile
```

-	Layers:
	-	`sha256:0ab095411675418e44e21c84783da6d13083781e1fe97497fc7e2f5b621ca02e`  
		Last Modified: Wed, 24 Apr 2024 02:21:59 GMT  
		Size: 839.5 KB (839491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:accafe341d8b602c7d62833c2c4574413092a5e748c5a085501cb3486f14d271`  
		Last Modified: Wed, 24 Apr 2024 02:21:59 GMT  
		Size: 30.1 KB (30102 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:7d82a4a1bef2436bf3a1461237888d58380cea7bb642a5d013f08e30dd33f78b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7262382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04757e24994ac38839a4c3e17f7ae2f52c3bb79d42be79ddcc913968c82c6939`
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

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:bc055aa29713367270a566b4778985111b6b388bd5e9fb10cf7d2ded1321166f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.6 KB (869600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87b69708eda874b56c620b0f9bc083e230cd37e088e782aa3d40047126fe89d`

```dockerfile
```

-	Layers:
	-	`sha256:e85eca891bbd005e842b8955c8555feee47b7733b7f40595abeb9f504d096162`  
		Last Modified: Mon, 06 May 2024 17:59:18 GMT  
		Size: 839.4 KB (839413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219169756931850cff20bdf77dc7d007775661b405b1310c87dd592e2a982a6a`  
		Last Modified: Mon, 06 May 2024 17:59:18 GMT  
		Size: 30.2 KB (30187 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:91adf72be7265453dc7b3e3ba8eaa9d9a8998287d67aa1c3d90f7a4af8ea1bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7406978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9a52a5721b2d5767b18936a8ff5afcdc99c4f63614e30f552219dcc0031dc0`
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

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:33979f46daaea0f9f1a3cbce47c319397436ff898421a1807aca78f8aa54f2ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.7 KB (867738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c334518f4c29c7a3cb0995425c8c5a827df9bb01a161450040d101d76fa2cbdd`

```dockerfile
```

-	Layers:
	-	`sha256:10ef38d8d10ae8263fc12a2405296fd4b2bc2f0fdc4055ff6130c50c53814541`  
		Last Modified: Mon, 06 May 2024 18:19:28 GMT  
		Size: 837.6 KB (837584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf8a0bb899d63922135accbb0f7c75646e71d87c2cf1115c893e71bd85d30ca8`  
		Last Modified: Mon, 06 May 2024 18:19:27 GMT  
		Size: 30.2 KB (30154 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:810f7640d7235fdfefb4c54834445b0e2490b5a25bf8297e35984c56c69d7574
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7206618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61143606f2893d760c7bb5f97a69eb036a51b329c2468b8b61d993ef964c5605`
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

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:633b6155d5ece991d7c50a68cfb46eebcae3e0bdc0a45c9438242c7c322bb892
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.6 KB (867593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f25f05a9bb0e21baf87b57601a0399695112bd0095641ffd00ba0fa71a3f41e`

```dockerfile
```

-	Layers:
	-	`sha256:b1a017a60774f9c8b4599aaa29c97bb0d8e77820e5f17d7c5b7cc2431cd0de7b`  
		Last Modified: Mon, 06 May 2024 18:14:40 GMT  
		Size: 837.5 KB (837514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1ff357c24f9ace748f0c0be3a7d756422f822077f86675c7929ee896b2c29f29`  
		Last Modified: Mon, 06 May 2024 18:14:40 GMT  
		Size: 30.1 KB (30079 bytes)  
		MIME: application/vnd.in-toto+json
