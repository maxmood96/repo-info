## `nginx:stable-alpine-slim`

```console
$ docker pull nginx@sha256:793fcc61c7d3d94669e650a8c38ac9fe25afd49769c0d3bf5faf4f4f823b8d4f
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

### `nginx:stable-alpine-slim` - linux; amd64

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

### `nginx:stable-alpine-slim` - unknown; unknown

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

### `nginx:stable-alpine-slim` - linux; arm variant v6

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

### `nginx:stable-alpine-slim` - unknown; unknown

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

### `nginx:stable-alpine-slim` - linux; arm variant v7

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

### `nginx:stable-alpine-slim` - unknown; unknown

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

### `nginx:stable-alpine-slim` - linux; arm64 variant v8

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

### `nginx:stable-alpine-slim` - unknown; unknown

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

### `nginx:stable-alpine-slim` - linux; 386

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

### `nginx:stable-alpine-slim` - unknown; unknown

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

### `nginx:stable-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:05ed26d31509e7e87f1e3c624052aa454ce8d30f66c00bfc6c5d294d681c9983
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5531415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:070b57042fd90a8c7c114a98e3ea6e1294d6136a5ffac7dbef1dd4d52c813217`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 05 Feb 2025 21:27:16 GMT
ENV PKG_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
ENV DYNPKG_RELEASE=2
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Feb 2025 21:27:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3e5207e2470174a8c60753afc8e1b66ed85e6250a9c6ec0625fc1f7d0a698a2`  
		Last Modified: Fri, 14 Feb 2025 19:45:30 GMT  
		Size: 2.0 MB (1951133 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39076361f14bee9cc0dde8d6e56f7b22deecf9efce7bd47c564b1995ed7930fa`  
		Last Modified: Fri, 14 Feb 2025 19:45:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:366f2af247e8a02c7c1e2d050e5967a735e6c5aceaf66b8bccdd21352f14e232`  
		Last Modified: Fri, 14 Feb 2025 19:45:29 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abc6cdf6a1285d65f04928fcc04930cdf44c4476762cf20a9cee617243ccd150`  
		Last Modified: Fri, 14 Feb 2025 19:45:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2d00788391a38066eef555ca1715025e9ff57ac997f8cd06214e217185da19e`  
		Last Modified: Fri, 14 Feb 2025 19:45:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a43e9d710ce03fd94c5cb71d57ba8e554d718f27b5d32f37d1579cbebd3cc6b4`  
		Last Modified: Fri, 14 Feb 2025 19:45:30 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6d4f18e1a55d9302771481d51dfcdff8381796c420e228193986bd701854c9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 KB (490726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e7e464592c2d99c62b00f3654859b84f4d193473e43264ee2124c102036174c`

```dockerfile
```

-	Layers:
	-	`sha256:8cd990acee1495d04f8a51e203412593f26cc19d1bc3e5de17c4d4aa9855b79c`  
		Last Modified: Fri, 14 Feb 2025 19:45:30 GMT  
		Size: 461.2 KB (461181 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:510ecc8ca74978d3aaef2f97e80e348da74d1f61c8b12a7f302abd23e4c891a5`  
		Last Modified: Fri, 14 Feb 2025 19:45:29 GMT  
		Size: 29.5 KB (29545 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:765f024e543b0d7c3df20693ee4b799547a427cec0a23752ac6ed8fd03fb8239
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5311771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f663f3899b56697d191d2b343ba186cab1c7942bc567486c458747befb005971`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.20.6-riscv64.tar.gz / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 05 Feb 2025 21:27:16 GMT
ENV PKG_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
ENV DYNPKG_RELEASE=2
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Feb 2025 21:27:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:69ccf1207daf2e3c381041f63cfe024189987fde3b1e97110475a71eac2581ba`  
		Last Modified: Fri, 14 Feb 2025 18:57:42 GMT  
		Size: 3.4 MB (3373232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:683874d204a49f0b02f27e45d113a12b583489af5f79a4dee173fb2f76a61e4b`  
		Last Modified: Fri, 14 Feb 2025 23:27:26 GMT  
		Size: 1.9 MB (1933934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8e5fd3cc5f713796274ff26cc5ed2b9cee18d6c7e3b25f78573c7c200e16123`  
		Last Modified: Fri, 14 Feb 2025 23:27:25 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a30f12a19704c33fe10738725365ef84acd718dd40e1eb4ac998e844b652e11`  
		Last Modified: Fri, 14 Feb 2025 23:27:25 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f993cf2842d4f4b37f11fd6339b30fb2b24d6f85b87a3434cbd60b46cd01bac2`  
		Last Modified: Fri, 14 Feb 2025 23:27:25 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2163a7e196a1f289c48d8911250d61b2949623814a92caa78dfe623eb80dd094`  
		Last Modified: Fri, 14 Feb 2025 23:27:26 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52412be8af802761a5da2c075079637d2719baa33be9c7ff06dab87b4cab5744`  
		Last Modified: Fri, 14 Feb 2025 23:27:26 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8cc26e57f9678a411fc5608fe9b61e25e4a5d1ae6cf90ddf1629ec3072046106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.7 KB (490722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c84de53724aa84ff42ba6969e8b7e7ad93e69b7034a21a3e21f9e4a715f4808`

```dockerfile
```

-	Layers:
	-	`sha256:818314304191f75bfbba1db4f672fb81895e73c73a44f43e98d8e6b662715219`  
		Last Modified: Fri, 14 Feb 2025 23:27:25 GMT  
		Size: 461.2 KB (461177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24990a04482723debbaff817b5dc0a9e126ce2922568bc1cf546ca812d13181a`  
		Last Modified: Fri, 14 Feb 2025 23:27:25 GMT  
		Size: 29.5 KB (29545 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:1f887005d4b79121cdf4af6bdfc586ef5edc380a20929256f54846f9ecf74ec9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5450995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6543234e28fe1e6ee0d7df0b9b9ef1189f5b473de9eb0439728f458a9b72ce90`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["/bin/sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NGINX_VERSION=1.26.3
# Wed, 05 Feb 2025 21:27:16 GMT
ENV PKG_RELEASE=1
# Wed, 05 Feb 2025 21:27:16 GMT
ENV DYNPKG_RELEASE=2
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"3a4e869eded0c71e92f522e94edffea7fbfb5e78886ea7e484342fa2e028c62099a67d08860c249bf93776da97b924225e0d849dbb4697b298afe5421d7d6fea *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Feb 2025 21:27:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1aafc7fae5f0e1e87307370987d708b9c005ba8d8a210cb7eac1fb9211b55433`  
		Last Modified: Fri, 14 Feb 2025 19:48:13 GMT  
		Size: 2.0 MB (1982270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f966cb342db91d97d802e6114f29c09c70ad1dfe6068b69f13ca1ef8a65e67`  
		Last Modified: Fri, 14 Feb 2025 19:48:13 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5c8bb5454c91a5a4d3abdeaee5e68610ce5f8929db47ae84630502145ef4aaa`  
		Last Modified: Fri, 14 Feb 2025 19:48:13 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab4162e1c49935e9e3b3e8624789c6b21b781661439a9fd9fb03797e839dad5e`  
		Last Modified: Fri, 14 Feb 2025 19:48:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5021f9cdd4e7b2f903f869651b5ef369ce3ccc1d8ade33d0f0b6c251b4004668`  
		Last Modified: Fri, 14 Feb 2025 19:48:14 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c6013e79396296a17f0a5291d65ab4a87a380ca519cd040db1541c1f0dde940`  
		Last Modified: Fri, 14 Feb 2025 19:48:14 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9224c623d1eb76b84b1b1fe5840599bf7dd9c83e9f2c5bcc36813d48c8227592
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **490.6 KB (490624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ececbe9c5b5642f36b2083410212218ea431a77b12295bb4ea870183ef5ca3c0`

```dockerfile
```

-	Layers:
	-	`sha256:f9308e23af2a4cd26c9b6077d55495871f98c415371a59352bdb6837181479f3`  
		Last Modified: Fri, 14 Feb 2025 19:48:13 GMT  
		Size: 461.1 KB (461135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:251c46580327792f35c77199f41ec1f13415b43acfc0e43d3eee78ece1480d9b`  
		Last Modified: Fri, 14 Feb 2025 19:48:13 GMT  
		Size: 29.5 KB (29489 bytes)  
		MIME: application/vnd.in-toto+json
