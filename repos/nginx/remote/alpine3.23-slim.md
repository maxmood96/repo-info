## `nginx:alpine3.23-slim`

```console
$ docker pull nginx@sha256:9f1f3f496bd5d223c374b5ad9a0b57e472c159c1d692ba3010f50cd1e68543a7
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

### `nginx:alpine3.23-slim` - linux; amd64

```console
$ docker pull nginx@sha256:f27729b79d1b60ba78fee853d4bbf51e62d45d630cbb522923c13df3303ec66a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5719926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52264b0bf8450c8c2cba89444e139d66dc5c40ce77f3c8db4067f9dd9a6d6688`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86_64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 22:51:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 22:51:33 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 09 Dec 2025 22:51:33 GMT
ENV PKG_RELEASE=1
# Tue, 09 Dec 2025 22:51:33 GMT
ENV DYNPKG_RELEASE=1
# Tue, 09 Dec 2025 22:51:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 22:51:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 22:51:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:51:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 22:51:33 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:014e56e613968f73cce0858124ca5fbc601d7888099969a4eea69f31dcd71a53`  
		Last Modified: Wed, 03 Dec 2025 19:30:44 GMT  
		Size: 3.9 MB (3859315 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfad290a5c259f8d1ec1938529f8ef602e335a26680497ad56d38e0727e1a10a`  
		Last Modified: Tue, 09 Dec 2025 22:52:02 GMT  
		Size: 1.9 MB (1856020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d2cc344426d3d91200b457a771ecfe976de824e165506f5cce5d6b863da1ca9`  
		Last Modified: Tue, 09 Dec 2025 22:52:03 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abdece946203a31d986f184559f417a33c3a8936a80153b2f0ffa208af4a0d48`  
		Last Modified: Tue, 09 Dec 2025 22:52:03 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51c30493937c33bd8b568d8aed09d9596f558d08877b05a5e1855516aba05e1f`  
		Last Modified: Tue, 09 Dec 2025 22:52:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad5b65da02cfbd43daa87443b87051f3816a10eb7719938d8cb9a96ee828d471`  
		Last Modified: Tue, 09 Dec 2025 22:52:03 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc13532503d72b70e7dd276ae52f2743b14326b83c31935c86d7477c66019dea`  
		Last Modified: Tue, 09 Dec 2025 22:52:01 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:0dfc5c284eb24c41999b16ad3ce0ff43bb5fc002e846ba754fa671ac385bebb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.9 KB (502851 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bb60a9455aea53ec6b950eb32e8e901e2678221e8149375b321dc8868c88956`

```dockerfile
```

-	Layers:
	-	`sha256:4135fb3d40439cac2ffdcbd7d525a3fdb193a42a39e2118810978c0fd25a64c1`  
		Last Modified: Wed, 10 Dec 2025 00:52:16 GMT  
		Size: 474.0 KB (473984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f651800c39f5a0a0a8fc7ed3b50146913334255b0c72e6ac3be28c3f85d3e7d`  
		Last Modified: Wed, 10 Dec 2025 00:52:16 GMT  
		Size: 28.9 KB (28867 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:df304a32bf6a35a552a8327d05e8d663e07a80e02225c0b6f7097d29f499b1ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5426345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a09d2b4567fe959b2a1277976bc920bf9feb54e05d594281e9771625bf0e3a4a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:25 GMT
ADD alpine-minirootfs-3.23.0-armhf.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:25 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 22:52:27 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 22:52:27 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 09 Dec 2025 22:52:27 GMT
ENV PKG_RELEASE=1
# Tue, 09 Dec 2025 22:52:27 GMT
ENV DYNPKG_RELEASE=1
# Tue, 09 Dec 2025 22:52:27 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:52:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 22:52:27 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:52:27 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:52:27 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:52:27 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:52:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 22:52:27 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:52:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 22:52:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:dd0740468c9e19d93d459e4637a652c4fb8e1012c1adeac2e7311f14dcd210f6`  
		Last Modified: Wed, 03 Dec 2025 19:30:39 GMT  
		Size: 3.6 MB (3567894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7533b2e4b31206a68c0d440f865d4708c51ada1273e31f7c06e8c603f3300ff9`  
		Last Modified: Tue, 09 Dec 2025 22:52:38 GMT  
		Size: 1.9 MB (1853848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c38972d9a17ca5abf9a4bc75a0d1b7942d244bf041c9e7b4a5d6e82481378973`  
		Last Modified: Tue, 09 Dec 2025 22:52:38 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4cea433b58c3ede570ab36f9c3152a662495b14a7212749e1141905da5920e`  
		Last Modified: Tue, 09 Dec 2025 22:52:38 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da6844d993e8fa01894712e5831c4e8a737fd95a2a0eaa21a3f3f35c4a0ca3b6`  
		Last Modified: Tue, 09 Dec 2025 22:52:38 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f72ca10f5868133c150e2acb3f14095eaa3395adfd2341bbf56063d274c78e6b`  
		Last Modified: Tue, 09 Dec 2025 22:52:38 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90de5bb911e157246d380c645d2ce15052a2b8014cb87ac61928b4153ec7f927`  
		Last Modified: Tue, 09 Dec 2025 22:52:38 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:90797e0b25b80ba12bbac5a33f64d0875b284b2db185127ec6f23369e5be197f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 KB (28779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a90d751bc53b500dcf1dddd50cc988eadf85ed288168f3bee3ea055847f591e`

```dockerfile
```

-	Layers:
	-	`sha256:074275d283f4d363604fa886393a53361e0737e8d4b7026eb6fbe5521415f477`  
		Last Modified: Wed, 10 Dec 2025 00:52:20 GMT  
		Size: 28.8 KB (28779 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:ffc683f51b4ddb463886b9da2b2090f1b5bf52c4667ef6501ce734b676918509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (4966072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f62503c093a48e71cfb505dccedeb9bd6a0c2da3867df32012f351a40a29234f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:51 GMT
ADD alpine-minirootfs-3.23.0-armv7.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:51 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 22:51:11 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 22:51:11 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 09 Dec 2025 22:51:11 GMT
ENV PKG_RELEASE=1
# Tue, 09 Dec 2025 22:51:11 GMT
ENV DYNPKG_RELEASE=1
# Tue, 09 Dec 2025 22:51:11 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:11 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 22:51:11 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:11 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:11 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:11 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:51:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 22:51:11 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:51:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 22:51:11 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5f34bcd7b3c0108b00e414f3370e9140a1cb6e02ec1caaa14ff2f25408910a24`  
		Last Modified: Wed, 03 Dec 2025 19:31:07 GMT  
		Size: 3.3 MB (3278466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed553162f0691018b2d95274823131163ff6a7abd69d651451ba60b818b7ee47`  
		Last Modified: Tue, 09 Dec 2025 22:51:25 GMT  
		Size: 1.7 MB (1683004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd6b891e835eb4714555088f1515c067cea86f0863fe9716fe4abba6dc7a1d1`  
		Last Modified: Tue, 09 Dec 2025 22:51:25 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5eb48c7295eb8e11dd8f6a68bd28d147cf7590ab79d476bbe09481fe5029adf`  
		Last Modified: Tue, 09 Dec 2025 22:51:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3313b8d36f49284ae7876e99a46f5b0be38f7ef0a8d2e27bf42bf33ff55a3c79`  
		Last Modified: Tue, 09 Dec 2025 22:51:25 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:817ee4998ab0d06cffb92badb6dd62eeb6cd3fe499bbd29690c64fbf5485d9a2`  
		Last Modified: Tue, 09 Dec 2025 22:51:25 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3a6742cb09b65950529fd27fc65bc3f2089cb19a96aed1b5bff86b17171f9f6`  
		Last Modified: Tue, 09 Dec 2025 22:51:25 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:eb7b323bae68c8c6957660ca4ad00890784da364e2744c893973dfd71ca46457
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4099433a4291e5db43c35b70ee14a028a447263c48ac34739ecb53155763d6e6`

```dockerfile
```

-	Layers:
	-	`sha256:4229ec2e2267b34476eba392654ef05a5d64807fd127a9e5b6137759a7086163`  
		Last Modified: Wed, 10 Dec 2025 00:52:24 GMT  
		Size: 473.4 KB (473418 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:34d8f1a8e10ad7a52dfed205acc290b0c3b298722333c7b2be5b96040be3cd84`  
		Last Modified: Wed, 10 Dec 2025 00:52:25 GMT  
		Size: 29.0 KB (28995 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:b26e58b35344da60e494a659d2a8e9c82d2492209cf3c5eb8f31473b1959e22d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.1 MB (6072630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081b26ea1f776e67c1896387839460b9977b59d4e6ca6bb5329f567c5bf4168d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:17 GMT
ADD alpine-minirootfs-3.23.0-aarch64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:17 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 22:50:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 22:50:39 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 09 Dec 2025 22:50:39 GMT
ENV PKG_RELEASE=1
# Tue, 09 Dec 2025 22:50:39 GMT
ENV DYNPKG_RELEASE=1
# Tue, 09 Dec 2025 22:50:39 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 22:50:39 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:39 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:39 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:39 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 22:50:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:50:39 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 22:50:39 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0bd713040ebbdef7247f70b0753f8fb2f410e8eb358e95af409a8412b9847d78`  
		Last Modified: Wed, 03 Dec 2025 19:30:49 GMT  
		Size: 4.2 MB (4195200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d85e26d0c84da51ab7629f8b46bde1a9b8158beded40b33a75e696380ab864af`  
		Last Modified: Tue, 09 Dec 2025 22:50:51 GMT  
		Size: 1.9 MB (1872836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29b7c987abf6a201617f05404ba70e6921536e4ed49ee3727a5af3f2db987b79`  
		Last Modified: Tue, 09 Dec 2025 22:50:51 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6b7df06dc7618b5a5c6dd9878b9c56d4ea65624a16fa799aa8159afc01638fe`  
		Last Modified: Tue, 09 Dec 2025 22:50:51 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e350a0f963e3bc89893d212cb081562aea46364f51a07024ca3390b3bc2f565f`  
		Last Modified: Tue, 09 Dec 2025 22:50:51 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:223f9efb31593bded345c3e049812e1f38ac9618205651c693be3240a180fa73`  
		Last Modified: Tue, 09 Dec 2025 22:50:51 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2422bf7322776ff7b8f61a8ec3c425e4c297e898c974d4c89b394b88d14eac25`  
		Last Modified: Tue, 09 Dec 2025 22:50:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:f8e95ec08d7925123eb33b510beb8ece46103de601997b9e599f78871a585cac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.5 KB (502505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1c49e6e05d254247a7cdf8fcc58ffa580c825f7c5b0124c079c50b92ae2bd2`

```dockerfile
```

-	Layers:
	-	`sha256:898c7a1673ef2a3e1f519ccb26cf8a0f9719b35d86328035645dd4e8e833a22d`  
		Last Modified: Wed, 10 Dec 2025 00:52:28 GMT  
		Size: 473.5 KB (473462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fd879fa01d3d1d0e0dd9fb603f9d5d7751b744ec0c82724d8095fcbb56020c04`  
		Last Modified: Wed, 10 Dec 2025 00:52:29 GMT  
		Size: 29.0 KB (29043 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; 386

```console
$ docker pull nginx@sha256:4d8be79767ba35627d4fcfa7c34d6e2d2e2e36aee9aa162261b037b97f6bd289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5619971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:959c7e6d2fd02f11e80f34fad4c1b457b45a9d17d03ce48258f911a4666cadac`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 03 Dec 2025 19:30:18 GMT
ADD alpine-minirootfs-3.23.0-x86.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:30:18 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 22:53:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 22:53:05 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 09 Dec 2025 22:53:05 GMT
ENV PKG_RELEASE=1
# Tue, 09 Dec 2025 22:53:05 GMT
ENV DYNPKG_RELEASE=1
# Tue, 09 Dec 2025 22:53:05 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:53:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 22:53:05 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:53:05 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:53:05 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:53:05 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:53:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 22:53:05 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:53:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 22:53:05 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3527b4f952d5950d8caa74dc0d1759215000f2f0a195344f0239c7e2805fe2fc`  
		Last Modified: Wed, 03 Dec 2025 19:30:41 GMT  
		Size: 3.7 MB (3685856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2797262f12b78dccd98baa7fec7eb1224301ddfd26f73b5169e550a2fbf1c122`  
		Last Modified: Tue, 09 Dec 2025 22:53:18 GMT  
		Size: 1.9 MB (1929520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3826e3793d482d423faa7c7a3064b7c444ba7a99aa2cc83c92a8116a6120fbba`  
		Last Modified: Tue, 09 Dec 2025 22:53:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5317bdbc17f569f44fc1c67738f358cc8f8256fd394d405c7a56b9dd0984fb7f`  
		Last Modified: Tue, 09 Dec 2025 22:53:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b41a2c0cbc2304520c1711514d62c133359ed8676db81f4ea2531854e883a91`  
		Last Modified: Tue, 09 Dec 2025 22:53:18 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d2ae820e03ecbb19af0200e496db444f84eed812f48312652e6a673fec09b0b`  
		Last Modified: Tue, 09 Dec 2025 22:53:18 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6428409b961857c2950a8cb99eb057a5a277e24ccd2863af07f651b508f2ce57`  
		Last Modified: Tue, 09 Dec 2025 22:53:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:5d1c98510c2ec782901085892ea2522fee37b28d48bd4ed7db6efd3d3ee84be6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.7 KB (502734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f23568b7ad2e1edbf926e01e6a7feacc7c093791c5186958287762aafec68147`

```dockerfile
```

-	Layers:
	-	`sha256:3d8b819ca25270da213c59fae73cedab81105138311d9171978ce130c63c3c9f`  
		Last Modified: Wed, 10 Dec 2025 00:52:32 GMT  
		Size: 473.9 KB (473929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:19835dfef415e6756e37e065a5aec3997921ff728b14a51d4a33442fa97a0854`  
		Last Modified: Wed, 10 Dec 2025 00:52:33 GMT  
		Size: 28.8 KB (28805 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:909dfdf37bff8e72425c1d6d75091e630d55bfac869df91e1d5893735f7309ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 MB (5778779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a4bf9f61828321004194c2c4dec6582f4f66e94f415e552e760c27568ffaeeb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:24 GMT
ADD alpine-minirootfs-3.23.0-ppc64le.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:24 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 22:50:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 22:50:19 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 09 Dec 2025 22:50:19 GMT
ENV PKG_RELEASE=1
# Tue, 09 Dec 2025 22:50:19 GMT
ENV DYNPKG_RELEASE=1
# Tue, 09 Dec 2025 22:50:19 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 22:50:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:22 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:23 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 22:50:23 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:50:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 22:50:23 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bebb36295c11d2d52cd92944b382c4aa60dce148b63090816248052f38358488`  
		Last Modified: Wed, 03 Dec 2025 19:29:52 GMT  
		Size: 3.8 MB (3827017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7a97bf32984bcd97ee8061569eea49090558d371900c8a75f2a55f730e8bb8`  
		Last Modified: Tue, 09 Dec 2025 22:50:54 GMT  
		Size: 1.9 MB (1947169 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a01fc92880c6aab68b5c1e82be54d5aea49fbec0f8d5a44b7f2ee855d8d6408`  
		Last Modified: Tue, 09 Dec 2025 22:50:54 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f8a2dba1736e4185c2e5e94b23149b95cb2b18d107f5e0624b4cfa7db7ac08`  
		Last Modified: Tue, 09 Dec 2025 22:50:54 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f59be2dcb3528d33475a12fb38eb933fec9a1a44166624da2315aa1edf52263`  
		Last Modified: Tue, 09 Dec 2025 22:50:54 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f87a7f593f18348a59593af5fbb2ca34fbb4b11e88dae3a86eb1581c7bd367e3`  
		Last Modified: Tue, 09 Dec 2025 22:50:54 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c032e183d46a8a989911f7fbd566f87b5a6250e879d1f877387d8964743ae35`  
		Last Modified: Tue, 09 Dec 2025 22:50:54 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:44d4c1a41987a4af08e690aa46a7f3b10a4e52dcce777b8ffe1b9ca30471f3e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.3 KB (502349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b99c9435148d8f98da86cc54707bab29a7c802feb460050caef04982e72e48e`

```dockerfile
```

-	Layers:
	-	`sha256:5dfc63032c05792448525d647d770468767449f3e79d76f445fc4fcf0f3d25d6`  
		Last Modified: Wed, 10 Dec 2025 00:52:37 GMT  
		Size: 473.4 KB (473403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:187df7c4c5914afe1084799ed83fc389400d22558ee7a4827b732d3c00e89796`  
		Last Modified: Wed, 10 Dec 2025 00:52:37 GMT  
		Size: 28.9 KB (28946 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine3.23-slim` - linux; s390x

```console
$ docker pull nginx@sha256:6f5e472ce4aa8e4904cd81369bbe713c092113d5e47dfef883b57810f9453e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.7 MB (5700965 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f7da34edd828e1914dddc3c398bf589356092c4f23229cba839e1fdc38a9e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:31 GMT
ADD alpine-minirootfs-3.23.0-s390x.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:31 GMT
CMD ["/bin/sh"]
# Tue, 09 Dec 2025 22:50:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Dec 2025 22:50:17 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 09 Dec 2025 22:50:17 GMT
ENV PKG_RELEASE=1
# Tue, 09 Dec 2025 22:50:17 GMT
ENV DYNPKG_RELEASE=1
# Tue, 09 Dec 2025 22:50:17 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 09 Dec 2025 22:50:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 09 Dec 2025 22:50:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Dec 2025 22:50:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 09 Dec 2025 22:50:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Dec 2025 22:50:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c7cee97a7811b4965924727bdc0a2333d48e3c6b4064a9c8867d48607fa0fc16`  
		Last Modified: Wed, 03 Dec 2025 19:30:00 GMT  
		Size: 3.7 MB (3723810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d172289af8e12cb214e8ccdb4f8f698a993118d3ae21981987ce6fc75c5ffebd`  
		Last Modified: Tue, 09 Dec 2025 22:50:36 GMT  
		Size: 2.0 MB (1972558 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2e8a07b8456c9f5aaecb0aa40396becd082d432cb6a229d6acd539a1092a53a`  
		Last Modified: Tue, 09 Dec 2025 22:50:35 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3eeb9b64054e037efe9aafb6264c4056db8518dcea2a8730c8240602c98aec`  
		Last Modified: Tue, 09 Dec 2025 22:50:35 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb77efc8d230931c1faad9aeb5d50301a6d56dbc5ce698213f483a66822db58`  
		Last Modified: Tue, 09 Dec 2025 22:50:35 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ed1a4128358ba15f8b70d20d3d78c84a821f57c128f60c1eb3f667dfae6a3e4`  
		Last Modified: Tue, 09 Dec 2025 22:50:35 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b11b210e70df83aed4262b558746bb270b01fa5359bc5359b3249ad7eea9cc54`  
		Last Modified: Tue, 09 Dec 2025 22:50:35 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine3.23-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:77af0e6031da53c6a3f29f1f4adb17c1f51150ea120a16b85054b3bd4bcadb0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.2 KB (502200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c172b4b09030e4597bfbfd60eee23cfcb24e24f2b330ed87ef3fd495c762fce7`

```dockerfile
```

-	Layers:
	-	`sha256:f2a8d3ec90cfcb72e5a3b6ccfef955392550930a1b343c935d51c8fee700fd5f`  
		Last Modified: Wed, 10 Dec 2025 00:52:41 GMT  
		Size: 473.3 KB (473333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff6858cc4977046487c4455c1a178b3da6588fd6665ac93d48d0442337adb161`  
		Last Modified: Wed, 10 Dec 2025 00:52:42 GMT  
		Size: 28.9 KB (28867 bytes)  
		MIME: application/vnd.in-toto+json
