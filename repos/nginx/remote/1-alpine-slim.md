## `nginx:1-alpine-slim`

```console
$ docker pull nginx@sha256:94f1c83ea210e0568f87884517b4fe9a39c74b7677e0ad3de72700cfa3da7268
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

### `nginx:1-alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:94f11b88c5d30105df2236d818a2dd50577bd2314f70374ae53ccaec61ac34f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5609950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88c76efe46824dabc1a11306985e281a5c779ca367913691751d28327bf4df5d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86_64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9824c27679d3b27c5e1cb00a73adb6f4f8d556994111c12db3c5d61a0c843df8`  
		Last Modified: Tue, 15 Jul 2025 19:00:01 GMT  
		Size: 3.8 MB (3799689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bc572a340ecbc60aca0c624f76b32de0b073d5efa4fa1e0b6d9da6405976946`  
		Last Modified: Wed, 13 Aug 2025 18:52:42 GMT  
		Size: 1.8 MB (1805666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:403e3f251637881bbdc5fb06df8da55c149c00ccb0addbcb7839fa4ad60dfd04`  
		Last Modified: Wed, 13 Aug 2025 18:52:42 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9adfbae99cb79774fdc14ca03a0a0154b8c199a69f69316bcfce64b07f80719f`  
		Last Modified: Wed, 13 Aug 2025 18:52:42 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8a46741e18ed98437271669138116163f14596f411c1948fd7836e39f1afea`  
		Last Modified: Wed, 13 Aug 2025 18:52:42 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ebe2ff2d2cd981811cefb6df49a116da6074c770c07ee86a6ae2ebe7eee926`  
		Last Modified: Wed, 13 Aug 2025 18:52:43 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a992fbc61ecc9d8291c27f9add7b8a07d374c06a435d4734519b634762cf1c51`  
		Last Modified: Wed, 13 Aug 2025 18:52:43 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:875d14ca2844f4655f6cd5377bae9d1469993ce8798a4ede89ecef0e5b62d259
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.2 KB (504201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc01f487268695afc62798b7dafb2723a4c65144275ea13d731a85f0cd0095a5`

```dockerfile
```

-	Layers:
	-	`sha256:646d99c0f7bd9d357f7f78cc0d200f6ce516e68791e7ec1d861b0da7c564e0ae`  
		Last Modified: Wed, 13 Aug 2025 20:51:05 GMT  
		Size: 475.3 KB (475291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0fbd8c2acb848b7af9d93df641df15f9312188ef7e9403ff62e89f9bba5ce60`  
		Last Modified: Wed, 13 Aug 2025 20:51:06 GMT  
		Size: 28.9 KB (28910 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:b5cbc16fa02ea980f4b6b87c342cad17f26c17d14f3b2385efcbbd93f694318d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5307169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadcba44d87637d09250209f47d21c4ab1ca06040f939fafb06650d5c3e5458a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armhf.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:06bab5e847c5674d6ec26b342cc11d7a051a6a231e5db8a955d57bc9f4ab5595`  
		Last Modified: Tue, 15 Jul 2025 18:59:34 GMT  
		Size: 3.5 MB (3500910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28ccf18437923531da3f89aaacc91d4ec12b2156ad7187e32fac7e19431cbfa3`  
		Last Modified: Wed, 13 Aug 2025 18:54:02 GMT  
		Size: 1.8 MB (1801659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8bf702f5fc942faa88791d0cd953478c89484dd106decee87a4132f1992a02`  
		Last Modified: Wed, 13 Aug 2025 18:59:36 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0eb7acc3feec9009f8b48feb050b97d52247c545394642d6e5d7ecf1854374b7`  
		Last Modified: Wed, 13 Aug 2025 18:59:40 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd453b2e404562337a154b8aa1052089a6a1abb49290ad0220d74113f22e9ae`  
		Last Modified: Wed, 13 Aug 2025 18:59:43 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd304019335ebcee5f69c4fdccca5721aea08a17fcbe4e2d2d583cdfc37c8983`  
		Last Modified: Wed, 13 Aug 2025 18:59:47 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da401ace5c724355712e66e05910188e8fd4d774e972fefe1a66fc491f412644`  
		Last Modified: Wed, 13 Aug 2025 18:59:50 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:ce4ce80174a276bc6143668f41f469ff7ca089ff622481e484368349f32efb46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 KB (28819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1ee52e24399f77c176f686614cee4812456320403ff1f1e1da135ad362beb43`

```dockerfile
```

-	Layers:
	-	`sha256:dd9646c331206f8e1c11069efe2d88ee8a4de9e9e3393e809f9b146561d48f12`  
		Last Modified: Wed, 13 Aug 2025 20:51:10 GMT  
		Size: 28.8 KB (28819 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b8bf35e117567406e260d8ee77d2731004308b45c097a8c804d3fb078dca1327
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4860928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39908e0f49b6774bbfdc82dcd020de11813df94842d81099644dd4e385940f50`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-armv7.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5ee064f8764b09a64829b58705219a88e0b13243f7f403d66ac0c639640426a5`  
		Last Modified: Tue, 15 Jul 2025 19:04:18 GMT  
		Size: 3.2 MB (3219038 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c4c1483fd46a686c1b60d1dd7b370ed346acf8a34692db23d74bec2b859f51`  
		Last Modified: Thu, 14 Aug 2025 03:57:56 GMT  
		Size: 1.6 MB (1637296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80ad6eb3000e78abb6f7bd4536bb3e19c1b779af23643a055265384f2a69f54`  
		Last Modified: Thu, 14 Aug 2025 03:57:55 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:570cf126c657327998b3c6fb58ae637b0ff0553300c887333d9964022d600422`  
		Last Modified: Thu, 14 Aug 2025 03:57:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e71f25b5f32ed2da532b9965f6298f50ae8c764a15ad5af1a4be9db06584efa`  
		Last Modified: Thu, 14 Aug 2025 03:57:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4153b591fbedc06dfd92b0d399ce53247893c7c0a88e1bbcb4d83c20edf01ee`  
		Last Modified: Thu, 14 Aug 2025 03:57:56 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f262da183f0cd21c7b9ac80c17ae6806f053ef93caddcbec1c8e79095ed9cb`  
		Last Modified: Thu, 14 Aug 2025 03:57:56 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3244edb0ddcbdabef7ddd46ff6b5f92326add91103aad59caf9ae445570bc210
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.4 KB (504409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3dc876c1da74b9cfeb2b778ac8a6957da907ac10098b5b87f55c20c337aee37`

```dockerfile
```

-	Layers:
	-	`sha256:239df6242a415796333090ca8dacc9cf409fdf640c61dc42a704bc3911970837`  
		Last Modified: Thu, 14 Aug 2025 05:50:43 GMT  
		Size: 475.4 KB (475375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:302076f03d4a34e2d5b8e9831174dec520be737a90dbf09da6102cd36bbd796d`  
		Last Modified: Thu, 14 Aug 2025 05:50:44 GMT  
		Size: 29.0 KB (29034 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:c077b39a5004186e6ed5601a59f1cff3b807001a0f60c8098f6d272105bd4cf0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5935845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1fb71cb29f615de01a7c5ea9ba7db0de088250cb9a33d1b9aed59ee49ef5b69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-aarch64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6e174226ea690ced550e5641249a412cdbefd2d09871f3e64ab52137a54ba606`  
		Last Modified: Tue, 15 Jul 2025 18:59:50 GMT  
		Size: 4.1 MB (4130750 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f3b06c840fcb4c48cf9bfe1da039269b88c682942434e2bf8b266d3acdd4fd`  
		Last Modified: Wed, 13 Aug 2025 20:42:51 GMT  
		Size: 1.8 MB (1800509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ba7957f9d23b5a6073e2690367274e07226e16229a3874c65e854a457ca4d2`  
		Last Modified: Wed, 13 Aug 2025 20:42:51 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6156ecb6dfff3c433e78d41dab6d6dd7d2c5c759f6faebb49c0b6bc04874509b`  
		Last Modified: Wed, 13 Aug 2025 20:42:51 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bc2f07fbf03f53f2569fbdf75ab4c409fbde0d5ab4b4a6d49e8bfbd41577b76`  
		Last Modified: Wed, 13 Aug 2025 20:42:51 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c2c01fdb0949fef1a50f981f1c837eb1076c7731fbbcc3382fe699c33f232c6`  
		Last Modified: Wed, 13 Aug 2025 20:42:52 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66ce170f7dd87f4ee563e53b9f099a4e295f5e52cd580b4b84df4d3879c41486`  
		Last Modified: Wed, 13 Aug 2025 20:42:52 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:89812b1082ab84cffa886c4be279c4c72f0bc8b68f0a01b2dcb07294f187670c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.5 KB (504505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6e5c3d6aa5b26a3bf55bbc699b783c9509850db378453c1605d3517d118ef7`

```dockerfile
```

-	Layers:
	-	`sha256:651d7d9e60ec370aaba2dda0962283959fe271e885c5b389e117341b87a20057`  
		Last Modified: Wed, 13 Aug 2025 23:50:48 GMT  
		Size: 475.4 KB (475419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6e807bae8b351187520ae4a6d239ede2e502a367b74f5b3e937ec9165144f249`  
		Last Modified: Wed, 13 Aug 2025 23:50:49 GMT  
		Size: 29.1 KB (29086 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:a3a3f799a87829d1d661d74fc52832880e6976efd21af26143e8e13ab9215c58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5493573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9910e9095b852f81194916fc21f77e95ab9b5a6cd03b23f5e41e88cfc924ad18`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-x86.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a55f2fb89da4caae0d783c0045a67446dee9bbd977fecb44db9e1231550fa888`  
		Last Modified: Tue, 15 Jul 2025 19:04:11 GMT  
		Size: 3.6 MB (3615006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3208f52f360e091a3bd0401ef2da5ec3f54addd7e041fb51e7e57def8baf75b7`  
		Last Modified: Wed, 13 Aug 2025 18:58:17 GMT  
		Size: 1.9 MB (1873967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c150459bba47aa81ee2c082ec2633c1f8ef2aa11e561a2c09d1a4ee59c6b2ec1`  
		Last Modified: Wed, 13 Aug 2025 18:58:17 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15efc3e544937602a8f6d46ac99f12652ae0f3498ec3e013663e3919d80cdf38`  
		Last Modified: Wed, 13 Aug 2025 18:58:16 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:459b1386f212404cfade900491c47bd61a17996fdb60915c9fbd3734ed744875`  
		Last Modified: Wed, 13 Aug 2025 18:58:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7e4319561a90d2c89427cbba87476a8583873f0fd44611a9270ca22d79bb08`  
		Last Modified: Wed, 13 Aug 2025 18:58:24 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5166afe3b85cd858d36ef974ca4a60d067b0451989dcae92e00703b3f7b18f8`  
		Last Modified: Wed, 13 Aug 2025 18:58:16 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3625b8d00d8d4d0d4cbb879c841be0b98f906c017a551a207da965ef9d43d769
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.1 KB (504084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1dc1c5f7d14c56e3f2cb226cb948f0001c4f0d6628e85402e19d791a79fdbcee`

```dockerfile
```

-	Layers:
	-	`sha256:ba9368961612a476006bc0a29932c322349023df001b0b81eb41d337200adaa5`  
		Last Modified: Wed, 13 Aug 2025 20:51:18 GMT  
		Size: 475.2 KB (475236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd182bf6cfe08fbf90f313e5c4398c9eda5c22bb776dba715e52cd268fa07469`  
		Last Modified: Wed, 13 Aug 2025 20:51:19 GMT  
		Size: 28.8 KB (28848 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:6e154a65aa5e99bafcdf1bdfc11d00a2f70bde2ca7c40508af94ebe83c968a88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5597909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c0d3571ba136674df45bcd15bd8c0ff1b4aa38f456c361c86f9e93de3b1b778`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-ppc64le.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b762f678859bfa5c3948b5f1b04959aa43c8aba88e2389e281413d303d62a7e3`  
		Last Modified: Tue, 15 Jul 2025 18:59:53 GMT  
		Size: 3.7 MB (3727111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603b6089cd20f000d6ca370086e1665d34814e72c919f7185034e422d5171267`  
		Last Modified: Wed, 13 Aug 2025 21:01:14 GMT  
		Size: 1.9 MB (1866200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39414c0e493ba38592efc448581ea4f3740897e43445a59f09ad5cd87ee72b42`  
		Last Modified: Wed, 13 Aug 2025 21:01:14 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb25b471c1ece98244c3a225f05d9cad627f26c1c5087a44470ccc6753484489`  
		Last Modified: Wed, 13 Aug 2025 21:01:14 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29415cf098ea86aab0e956a181128dc94e20efea7cc8ca3d76f23433d3c8535b`  
		Last Modified: Wed, 13 Aug 2025 21:01:15 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75fe831da212af132370036a1e3d4df36aa300d9ac0bbfb0b7b4f4c62ec05d48`  
		Last Modified: Wed, 13 Aug 2025 21:01:14 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de23b4e2cb61364e435265d5735a4de601490f2a87169251d47114df2c134edd`  
		Last Modified: Wed, 13 Aug 2025 21:01:15 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:dabf4012bcf5051e4b281dccae0caf375f8889cbffeb9cd2420239b47be1ec39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33eab283a005f3db575cc96a6ef071c2e29eea8d9d6e4d4522626b86ee5edf06`

```dockerfile
```

-	Layers:
	-	`sha256:533ea474820091fc38fecae40e202fca333fbbc7c668ee9667d245714c00ac41`  
		Last Modified: Wed, 13 Aug 2025 23:50:55 GMT  
		Size: 473.4 KB (473410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35afb196196f85da662349333d4538ce7076e55c33d503a9632cd80361fc8b27`  
		Last Modified: Wed, 13 Aug 2025 23:50:56 GMT  
		Size: 29.0 KB (28990 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:0c8d0f105f18c21e7a378f8479fd58975e43ae914155cbd026ad3f3b85ec2e32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d15f4d75cdd3f3b99af5a9075aec865269bd92fcb34c405b1aed4dc4051ee73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-riscv64.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:cbe7080b5783de104ad67ff4595bfa8ae70a597181a84621f51c5ccd084218da`  
		Last Modified: Tue, 15 Jul 2025 19:00:17 GMT  
		Size: 3.5 MB (3512801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a58d354f0da45ce0af9a84c8b4643554e3f257990743ea21ca2cab9aa6552f9b`  
		Last Modified: Fri, 15 Aug 2025 10:19:01 GMT  
		Size: 1.8 MB (1846503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c7b3fd4610e3abf5b6540800b148e078a3e06efa9ebc210dc252058b93f622a`  
		Last Modified: Fri, 15 Aug 2025 10:19:01 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56137ef6a98603b2c28abe00b556776d31838cd64c26d5733fc7ebc970e93938`  
		Last Modified: Fri, 15 Aug 2025 10:19:01 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6169661b54b1cad5b6a1bd09519018b09a5d1cd12514fc01e9c593b1aa4958f4`  
		Last Modified: Fri, 15 Aug 2025 10:19:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d5bd8890dee7317d2ce5fab5b1f1c1f84a5baaf7a280ec8f8d68b2515c2f62`  
		Last Modified: Fri, 15 Aug 2025 10:19:01 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4548cbd1d41aa7d472be62da315d9ce1fb6d7e0ef926283a599ad8aad21a81d`  
		Last Modified: Fri, 15 Aug 2025 10:19:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8b71aecf14f478eba7d2278715f4c4ab21f7944625cd6f6ee0631f95311db6a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50e181c03938660179d2796dbd08d9e4c1e586b0f74675cdb6ab70066305d3af`

```dockerfile
```

-	Layers:
	-	`sha256:1c6bc867bf4bc9e433ff8b937a8592e205602463ba2222be4247b65a4c25381c`  
		Last Modified: Fri, 15 Aug 2025 11:50:36 GMT  
		Size: 473.4 KB (473406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:101831285bcb8fc45147644b5b1863b3a414b47e01c7ce9302ec09df0015013d`  
		Last Modified: Fri, 15 Aug 2025 11:50:37 GMT  
		Size: 29.0 KB (28990 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:738d26ea6a1da9b8914a7b0ae3ed745ff090d03dafa0c8d25b478fe196ba23b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5556583 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ad79b7d5fa95374abf39e5a0ffaf317417009cd480acb26c0d664e326d4e02e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 15 Jul 2025 11:01:16 GMT
ADD alpine-minirootfs-3.22.1-s390x.tar.gz / # buildkit
# Tue, 15 Jul 2025 11:01:16 GMT
CMD ["/bin/sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 Aug 2025 16:34:01 GMT
ENV NGINX_VERSION=1.29.1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV PKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
ENV DYNPKG_RELEASE=1
# Wed, 13 Aug 2025 16:34:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"43ecd667d9039c9ab0fab9068c16b37825b15f7d4ef6ea8f36a41378bdf1a198463c751f8b76cfe2aef7ffa8dd9f88f180b958a8189d770258b5a97dc302daf4 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 Aug 2025 16:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 Aug 2025 16:34:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 Aug 2025 16:34:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 Aug 2025 16:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5d29754ce036967079405405a04a54a7d3f8ba85e0057b6bdda3d03aa59c8361`  
		Last Modified: Tue, 15 Jul 2025 19:00:06 GMT  
		Size: 3.6 MB (3644971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d036a2a4aad5bbf4364895d5e42b093a9af43cb0d56946b185b8be6d574927ee`  
		Last Modified: Thu, 14 Aug 2025 03:15:34 GMT  
		Size: 1.9 MB (1907009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62494343380c68cc99c90b1ed1339988a4c6ea9f16354326cebb770e9ca46a38`  
		Last Modified: Thu, 14 Aug 2025 03:15:40 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77429e315ac77e60b6ec73256263b82d61a640db1385700d0d7767bb303cce76`  
		Last Modified: Thu, 14 Aug 2025 03:15:44 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f494288ab981c9c8ca49d865c64515aa46e49cf8c548ee32dd0549d8e2a66211`  
		Last Modified: Thu, 14 Aug 2025 03:15:46 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e7e167390a4f1386d8196cf3a3974cb9fb856cc64e6df6c6c2f8ddc1b7d6a6`  
		Last Modified: Thu, 14 Aug 2025 03:15:50 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2414e76fe2f1b643e8d6a720153ef0a4367a3c5baa6caa700e89eb6d5353b43`  
		Last Modified: Thu, 14 Aug 2025 03:15:53 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b553fd8f744175fc8165ad7dc68263a91b5c7419ad9fa6d7a6611a3688f29eaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.2 KB (502250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73b7985c0066f84b13520bc57f2b0234877817e0d1e8606c98eda2f7ee51618f`

```dockerfile
```

-	Layers:
	-	`sha256:cc54cd14861ed888bfb16f5abc54ea48f09e46cdf473c08667af146ae5ef2c6a`  
		Last Modified: Thu, 14 Aug 2025 05:50:56 GMT  
		Size: 473.3 KB (473340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a182a33f0ba10704221896f49e54bafb8ca0db0f8a4ee92dc6b4e122b960b45`  
		Last Modified: Thu, 14 Aug 2025 05:50:56 GMT  
		Size: 28.9 KB (28910 bytes)  
		MIME: application/vnd.in-toto+json
