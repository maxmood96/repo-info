## `nginx:stable-alpine3.20-slim`

```console
$ docker pull nginx@sha256:6d4f5fb02763f731c06f3e246d4edf89c3a2bbc5dd72eab2b02bc55ef4b8600e
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
$ docker pull nginx@sha256:5dd272cb8634fcf16381b959244c644f236f9c1685a1d13e9f3c377767682316
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5387258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:357e3f017af9bafa4f4d5afd7f5a1878add75d332e4b8857db9db620bac19ed6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:45:25 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 16 Apr 2025 14:45:25 GMT
ENV PKG_RELEASE=1
# Wed, 16 Apr 2025 14:45:25 GMT
ENV DYNPKG_RELEASE=2
# Wed, 16 Apr 2025 14:45:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:45:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:45:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:914d0eaf60479e4b17101b02ed1e82400c02231d11c32276fb24867f5f39e97b`  
		Last Modified: Wed, 16 Apr 2025 17:01:51 GMT  
		Size: 1.8 MB (1755765 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e18ef93c435d9cd1c48d1ae900cf7e92ee61ae11be6b3bdefc899f4be8efad9`  
		Last Modified: Wed, 16 Apr 2025 17:01:50 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8651333baae33f196ce13e6d5cfcc16e276b640bbca95329625fbb6a3f13855`  
		Last Modified: Wed, 16 Apr 2025 17:01:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d987ab110a5ba4aebf9df7115759f01e8a5d8be0a70045f4dc7a5b959be1b04c`  
		Last Modified: Wed, 16 Apr 2025 17:01:50 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35c2aa19c882e9ca054353d84a4b58904f72807055c441be84f27401714f25d`  
		Last Modified: Wed, 16 Apr 2025 17:01:51 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7c661bcc4ef10a5e7ee3b4f80a8d77754a4e6b1a598271b70bd220d804316eb`  
		Last Modified: Wed, 16 Apr 2025 17:01:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c6278c626e3c3cb644d1c36125191bbecb509788630a6023e3b74a8a58a940ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 KB (493212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0febd4be5bfefbf280b1e56c88a2d2fdca490c261c80587823a96e3ef0c34da3`

```dockerfile
```

-	Layers:
	-	`sha256:6944f82b252fa5c19a76205bcf3a0515225f670f24763b4878b07d4e50d80ecb`  
		Last Modified: Wed, 16 Apr 2025 17:01:50 GMT  
		Size: 465.6 KB (465585 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d961480dd1e7f7369551708236ea52ee98343516aebc31e2a249ff3368a8574`  
		Last Modified: Wed, 16 Apr 2025 17:01:50 GMT  
		Size: 27.6 KB (27627 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:4517a088e52e79f1bb90b5ffbe1b57919788a6ae5b2fc278998d866dffe8009b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5274339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31a71b9dc8e20279cb4fcd73757fd06d9a6cee01dc931addfe2036b8b204ade4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:45:25 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 16 Apr 2025 14:45:25 GMT
ENV PKG_RELEASE=1
# Wed, 16 Apr 2025 14:45:25 GMT
ENV DYNPKG_RELEASE=2
# Wed, 16 Apr 2025 14:45:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:45:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:45:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2c26bf5f8480a1434ff6e55ee1eacaaabc2f64a68470a58c5b046d8f5964745`  
		Last Modified: Wed, 16 Apr 2025 17:03:13 GMT  
		Size: 1.9 MB (1897209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25bdaedd96244e0ac6f152b3baba3954ff97a7340eed65a2babec3e0ae8bb6eb`  
		Last Modified: Wed, 16 Apr 2025 17:03:13 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f1dc84986dec4a11eda6445dddc07849ce36c3025bec2f026f58ae220b0d119`  
		Last Modified: Wed, 16 Apr 2025 17:03:12 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bdc8176553be71c3df47c76e7eb3c8045121942cf8b8515e8f32d464c7958ef`  
		Last Modified: Wed, 16 Apr 2025 17:03:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc394b2d85ee26f6b1bcb7631f435a0ef43735f7f39f8eb3d17c565243c01728`  
		Last Modified: Wed, 16 Apr 2025 17:03:13 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac031395267553539cb858c5ef0eff56bff92643e8ae61f061984f6e723a281`  
		Last Modified: Wed, 16 Apr 2025 17:03:14 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:d9230f3ad1130ffe8de10602c2b0c6b33b984ac83a5bfdce991c6cb37847735a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 KB (27504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad522fef5130e430cb7c9798c9f825cbd1374270814d2a3b59d72271026692e0`

```dockerfile
```

-	Layers:
	-	`sha256:090d037fc6c66a04107b5772dc81ab636d0324c9c3541ef60077d46a63e53042`  
		Last Modified: Wed, 16 Apr 2025 17:03:12 GMT  
		Size: 27.5 KB (27504 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:ecfc9b752f2127ac2288a067113827b5436f5e52dea521c4d864df423ca7cd60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4829276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6f08c7a36f7b5ac1041fa952df6b21067f2fd82581274c0ac928f264bc925b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:45:25 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 16 Apr 2025 14:45:25 GMT
ENV PKG_RELEASE=1
# Wed, 16 Apr 2025 14:45:25 GMT
ENV DYNPKG_RELEASE=2
# Wed, 16 Apr 2025 14:45:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:45:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:45:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf99db15f70b64ad3a26228487030375783084f6062b01ca4c65b3114476ee8`  
		Last Modified: Wed, 16 Apr 2025 17:08:57 GMT  
		Size: 1.7 MB (1728700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5054b2e2acc2991d8f0fb93c296faf9e2d375c05b52fa2a7e61a3f646bc7737`  
		Last Modified: Wed, 16 Apr 2025 17:08:57 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11f04eacde451536d60c8383a7ab6cc2e5947e0fc7c366bb9c1326167fa02fb8`  
		Last Modified: Wed, 16 Apr 2025 17:08:57 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e190b088ef4321c0c5e96358c8254dd108cf1a17521a4b11dc84b69b9afb7d3a`  
		Last Modified: Wed, 16 Apr 2025 17:08:57 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82aa7a5f21385f67d76de0e2097334e074e969358065e8371f06e910489eb5a9`  
		Last Modified: Wed, 16 Apr 2025 17:08:58 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:576d30ae104aae1ea27aab19814f2b13254cfac74c5d0c80eabebe2d0c9c112a`  
		Last Modified: Wed, 16 Apr 2025 17:08:58 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:28acaca75ab0133922386cebd920ef38557eb43bff64941a89aa1144dcbf8aa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.4 KB (493355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:228390f7b17812c65fe2ba75744a96a536c0911cbe28ecd883a2c3d87d94245a`

```dockerfile
```

-	Layers:
	-	`sha256:076729374760609f58a1777120de5b1b6db73dcde018add9529f5bef593c2f78`  
		Last Modified: Wed, 16 Apr 2025 17:08:57 GMT  
		Size: 465.6 KB (465637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:019536b2e48bcdc2d63bc6fb6ce3fae707f8c1e47cff690cce0855c906773fb3`  
		Last Modified: Wed, 16 Apr 2025 17:08:57 GMT  
		Size: 27.7 KB (27718 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:f5e2140c392fc11403dcbb2a21e0b921d651593084f2be07cee1899a2148c60b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5883803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:914a853699cb374cd81e39835bd4f17fe7a1cd0f00c749f0eec838df33738c08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:45:25 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 16 Apr 2025 14:45:25 GMT
ENV PKG_RELEASE=1
# Wed, 16 Apr 2025 14:45:25 GMT
ENV DYNPKG_RELEASE=2
# Wed, 16 Apr 2025 14:45:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:45:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:45:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b5b7a2d0351a33e1d34149cfd8d0cc4c7b3bbc6ecfee67809fe22ed10b33425`  
		Last Modified: Wed, 16 Apr 2025 17:02:09 GMT  
		Size: 1.8 MB (1788043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f7bb1290dbfa2b305786f6c84cb49c209de2afa4d149cbe0b4bfa050e925246`  
		Last Modified: Wed, 16 Apr 2025 17:02:09 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21b8c2c2584bcf9471f52b43f4fee4d54c7fb76517da72f07ff21a2439bc9125`  
		Last Modified: Wed, 16 Apr 2025 17:02:09 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014925e14361cfca96943aa9367c39a19fc6e806cbae3e1f30cd65bdc8bf46de`  
		Last Modified: Wed, 16 Apr 2025 17:02:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4431f52ff81db291b1025ec00511013b534349a0c740be431c48299ed5a088f0`  
		Last Modified: Wed, 16 Apr 2025 17:02:10 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca9948dfc2c8a0bda75fb117df98825d3b23ceae22003753f7485b8a912347a`  
		Last Modified: Wed, 16 Apr 2025 17:02:10 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9d876e4c0a5bd8f4e0415f73af730d0637d4861f63121f3f5e7b02b4498a5571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.4 KB (493420 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d367d7e359ebbf54bc149ab4aeee812c633cb8d237e814ba47bd80781e9c487a`

```dockerfile
```

-	Layers:
	-	`sha256:cf0978f14bbd479cb8edd074f58ec836330d93e145c206a412ae1a68d26bc156`  
		Last Modified: Wed, 16 Apr 2025 17:02:09 GMT  
		Size: 465.7 KB (465665 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d4626f2d887c90ed9d3d76434e448977736dfddb1794df008ba87b47be63088c`  
		Last Modified: Wed, 16 Apr 2025 17:02:09 GMT  
		Size: 27.8 KB (27755 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; 386

```console
$ docker pull nginx@sha256:772ff1c10470c7a5c18c1ee6a1508784a4c4968693832ff5db77c08f47071026
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:836410979a1f906991cc46a188015e7b95e3c38dbd4bef018ad134c5229ffcc4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:45:25 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 16 Apr 2025 14:45:25 GMT
ENV PKG_RELEASE=1
# Wed, 16 Apr 2025 14:45:25 GMT
ENV DYNPKG_RELEASE=2
# Wed, 16 Apr 2025 14:45:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:45:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:45:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f34d0189c51608f33f779e378b7cb6481147b231a08e95c8cfbe5c77d1641473`  
		Last Modified: Wed, 16 Apr 2025 17:03:18 GMT  
		Size: 2.0 MB (1962817 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d028b5736416ed97477229bacd6f5a10841e843cb0e16abda21352f9fc0953e6`  
		Last Modified: Wed, 16 Apr 2025 17:03:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d8d7b105c2cd6e97a43b23943c7e51b1858e3ae54648f61692558f94a6d278c`  
		Last Modified: Wed, 16 Apr 2025 17:03:18 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:548b70d6a930c2edae8954895d3a673fef39ca18af4acf378cf98838a681709f`  
		Last Modified: Wed, 16 Apr 2025 17:03:18 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c0517566dba67f92910a167596cdf1e9232e1c58bb6710c9ea62c96b6dd488b`  
		Last Modified: Wed, 16 Apr 2025 17:03:18 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc8989617e0d16b8d0c80609cd0a0b00c9a9cd35ec875ddd77c8dfec909a6867`  
		Last Modified: Wed, 16 Apr 2025 17:03:19 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:a1d0ebb1280f86cdbb5ee37a189065e24f7a1690116fedf3dc2766b7a370fc35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.1 KB (493135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b7c548463d6d96ea22484c678279a6d9421d27105422c2b1b903836d8c5922`

```dockerfile
```

-	Layers:
	-	`sha256:2e03ef87e00f92b4762194a316e948a03e102c72ed457b1b6631a6f7c098a813`  
		Last Modified: Wed, 16 Apr 2025 17:03:18 GMT  
		Size: 465.6 KB (465550 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:617392167996555573e3f3998858c15f2b4ab1bd52b297b010c50a2da0c00831`  
		Last Modified: Wed, 16 Apr 2025 17:03:18 GMT  
		Size: 27.6 KB (27585 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:353bd4047e6be354d454c42581582117852ecf68a3043aa3a0627e94c7a38d2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5533308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0d8d88288164b454b0d4886ccee4ea9ae5f0b7ba6701de310cd348b18e328b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:45:25 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 16 Apr 2025 14:45:25 GMT
ENV PKG_RELEASE=1
# Wed, 16 Apr 2025 14:45:25 GMT
ENV DYNPKG_RELEASE=2
# Wed, 16 Apr 2025 14:45:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:45:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:45:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0354bac33697408b7954104f7fb439383cf74fb7d789fb1ca4c958e860b1f6e7`  
		Last Modified: Wed, 16 Apr 2025 17:33:07 GMT  
		Size: 2.0 MB (1953028 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea0ac46725fc69ad83c98cd7bd142b042c431abd9efa668952795408cedf7dc`  
		Last Modified: Wed, 16 Apr 2025 17:33:07 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5cbf7930b6be8527d4dfab21a6a72268f12cc604d2625a1b1c4423a02bfed1c`  
		Last Modified: Wed, 16 Apr 2025 17:33:07 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5df26c8045614d4d8df96a60d21510ffc12f3e4744671613767b62fdc3fba45`  
		Last Modified: Wed, 16 Apr 2025 17:33:07 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c82e8af4bf32c6b7815cbf2b680c46271d7b69872d120a9491cbc0def3a0b090`  
		Last Modified: Wed, 16 Apr 2025 17:33:08 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767397833f65b2519194481b661edafb35e72ccc8eea09cbf5fbd143d71b8b2d`  
		Last Modified: Wed, 16 Apr 2025 17:33:08 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3524bfb4a4161eac829935de187d7bdb6bf02fffca372e694cc463b05ecc7e46
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.4 KB (491363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37ecbcc8b378d937642c7cff240c614bab4e0faa0ec1ab4e47cd434448c2b1d9`

```dockerfile
```

-	Layers:
	-	`sha256:94a591615e57d1b6fdcde8fa6b6ddf47f2a44d6341a89c99ad58eeb985dd4417`  
		Last Modified: Wed, 16 Apr 2025 17:33:07 GMT  
		Size: 463.7 KB (463680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77689b67fe3ad49a2e7121157ca3ed15177720a3ed1ceffef32733712aaa6552`  
		Last Modified: Wed, 16 Apr 2025 17:33:07 GMT  
		Size: 27.7 KB (27683 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:835328121081877d2e97aa9f0d42b480c13256a438bd1d1ce686529bc770a361
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5313720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74a0b13b9b5fc57a2e5f2711471f1488c5d9a76fe439e3a045efb5527d8a60b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:45:25 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 16 Apr 2025 14:45:25 GMT
ENV PKG_RELEASE=1
# Wed, 16 Apr 2025 14:45:25 GMT
ENV DYNPKG_RELEASE=2
# Wed, 16 Apr 2025 14:45:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:45:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:45:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:add9e4214eeb9c3c2135bb9c9cadd08dae43d8b2cad8777c363313e97d3befe1`  
		Last Modified: Wed, 16 Apr 2025 17:57:45 GMT  
		Size: 1.9 MB (1935892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877ff59fbcf8d54c935ff35faac62a63f37d65646e76098c94793b8e99f882b3`  
		Last Modified: Wed, 16 Apr 2025 17:57:45 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:254061367614b802e5c0c422e9a60d016d9cab71d519696dc8cf6ee4ed9a6aaf`  
		Last Modified: Wed, 16 Apr 2025 17:57:45 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:312baad9d2ba348f770f2c76ebce9c30c40f812820519956c72e228addce968f`  
		Last Modified: Wed, 16 Apr 2025 17:57:45 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3579a8e7111b6e2ed5900e91fc5a9b9458c5737ec897c40bca9fd010aab90c3`  
		Last Modified: Wed, 16 Apr 2025 17:57:46 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ea2971c0cae0121dd136f32efe5b0843a3523355c7e1bcd70a4fa4e809c083b`  
		Last Modified: Wed, 16 Apr 2025 17:57:46 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6af170a14ddfc8ab5957470623df3489050054e85198cc799f783b08580ba7f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.4 KB (491359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4e39993e5623ff5c93b60e94ca65eb84e1c3bb13684542899c184f30d27111`

```dockerfile
```

-	Layers:
	-	`sha256:dc7c0263e6678ff5a5c71015e79aa84196035eb43a1c77fae75ae461fbd5094b`  
		Last Modified: Wed, 16 Apr 2025 17:57:45 GMT  
		Size: 463.7 KB (463676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:10c226ce726b5aebe46ac8bd1461ef19051f209d0e7bf2a054b64f937bfad129`  
		Last Modified: Wed, 16 Apr 2025 17:57:45 GMT  
		Size: 27.7 KB (27683 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.20-slim` - linux; s390x

```console
$ docker pull nginx@sha256:7a2229a9137507d24e5da4aa59e9221e5a2c86539ec3fa252074b6365c9dc1ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5453004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:217f579167d0202bb494ba16a3665adadc5dcd9c1803b0c1d67bc5d828f814da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 14 Feb 2025 03:00:07 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Fri, 14 Feb 2025 03:00:07 GMT
CMD ["/bin/sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:45:25 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 16 Apr 2025 14:45:25 GMT
ENV PKG_RELEASE=1
# Wed, 16 Apr 2025 14:45:25 GMT
ENV DYNPKG_RELEASE=2
# Wed, 16 Apr 2025 14:45:25 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:45:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:45:25 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:45:25 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:45:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:591adf48b20a7b33c4636a66f81accdef249a063133961d7f7626783529127cc`  
		Last Modified: Wed, 16 Apr 2025 17:17:40 GMT  
		Size: 2.0 MB (1984275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9057490be6cf6c4ab6a8edc7f20715eaeba36bd9b0316b141d2b691cefc427d8`  
		Last Modified: Wed, 16 Apr 2025 17:17:40 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02247915cbb4ac8f7dad029b0f900a3083957ed81060a28a35f869b5231dd945`  
		Last Modified: Wed, 16 Apr 2025 17:17:40 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc48b9550f1d1bffc0646cab69d44b4d6b60c0f74fd4f27b01f7a10d2c2463e`  
		Last Modified: Wed, 16 Apr 2025 17:17:40 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e75428690c96cc36ea3c1bb8c107678813c1dd86d63352cf220f3f164c2449`  
		Last Modified: Wed, 16 Apr 2025 17:17:41 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fcc507f848ad34b472f5c5f815a307c49c34ffa332dab9662c5fc36a6b925e3`  
		Last Modified: Wed, 16 Apr 2025 17:17:41 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:87b96f99b24d3595970c9782ad2aebd964f18fd92b300a0e9184c5217a0baaeb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **491.3 KB (491261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da302b5b2d6c4cffccf83e5ae4400ce24af6656a4c13cc2cdeb3b17ad65e15fb`

```dockerfile
```

-	Layers:
	-	`sha256:c819f4d9e3cd92d59d1711d02322f02f86f8bb76d2183a1f6d0df104316c6635`  
		Last Modified: Wed, 16 Apr 2025 17:17:40 GMT  
		Size: 463.6 KB (463634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:224e05c2791a3497e99de55f0dbdd967d9cdb445d743f396a353911af0ff0da3`  
		Last Modified: Wed, 16 Apr 2025 17:17:40 GMT  
		Size: 27.6 KB (27627 bytes)  
		MIME: application/vnd.in-toto+json
