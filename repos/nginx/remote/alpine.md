## `nginx:alpine`

```console
$ docker pull nginx@sha256:052b75ab72f690f33debaa51c7e08d9b969a0447a133eb2b99cc905d9188cb2b
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

### `nginx:alpine` - linux; amd64

```console
$ docker pull nginx@sha256:e41316bb39937cebbf2674f26afe9e7bf94b4bbc6a301367891cf85843abfeda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22981575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a236f84b9d5d27fe4bf2bab07501cccdc8e16bb38a41f83e245216bbd2b61b5c`
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
# Tue, 09 Dec 2025 23:11:27 GMT
ENV NJS_VERSION=0.9.4
# Tue, 09 Dec 2025 23:11:27 GMT
ENV NJS_RELEASE=1
# Tue, 09 Dec 2025 23:11:27 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
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
	-	`sha256:136bc6976c2023e3363e66b88167d08019fece3e756c162c58754e3819bf4063`  
		Last Modified: Tue, 09 Dec 2025 23:11:39 GMT  
		Size: 17.3 MB (17261649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:95bfa8e026769d1f96b76b75d006e7979f5f730fe07975f183ae749763e8e700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.3 KB (905346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd37eff5c0390d8c0c2c920dcf0f27edbef3cd6ffb5045ece75eae262fbdacf`

```dockerfile
```

-	Layers:
	-	`sha256:1e626c7e7022ef92f00129e10c1a4163d80fc9f3ea332a7d8fd0f1f1e621c832`  
		Last Modified: Wed, 10 Dec 2025 00:51:12 GMT  
		Size: 884.2 KB (884249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a705e79f45b89d46a088c572da1398abbc94e73f9a8f13a4a5596307de4c8d7`  
		Last Modified: Wed, 10 Dec 2025 00:51:13 GMT  
		Size: 21.1 KB (21097 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine` - linux; arm variant v6

```console
$ docker pull nginx@sha256:8f32b0f6fada73c9df76ffa051a4a0481a67e62e82c06e357d56f9aca63ffdb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.6 MB (19572271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17906866f69921fee6c9d5eaccf900a6801f8f7f8c470d9d5183c47d7d9b57f6`
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
# Tue, 09 Dec 2025 23:11:20 GMT
ENV NJS_VERSION=0.9.4
# Tue, 09 Dec 2025 23:11:20 GMT
ENV NJS_RELEASE=1
# Tue, 09 Dec 2025 23:11:20 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
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
	-	`sha256:d527aaa3ea4328fcf101d34f5e453075cf17302004cfadac2fe94cbed7a1aaed`  
		Last Modified: Tue, 09 Dec 2025 23:11:33 GMT  
		Size: 14.1 MB (14145926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:6258a13ee324636bcc8f81367920c53f6329a02fa77783467ec21a0593b98ad6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.0 KB (21012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8babefbf403930c7934350e0d76ea97ec5e4e727f741735565fe05c6be838cb`

```dockerfile
```

-	Layers:
	-	`sha256:e07f60cba8c40fc78f5af92431894dddff581df19f03ccf57654e26aeb37f0ee`  
		Last Modified: Wed, 10 Dec 2025 00:51:17 GMT  
		Size: 21.0 KB (21012 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine` - linux; arm variant v7

```console
$ docker pull nginx@sha256:937ae6c577790c022767fb02f9c018c3875bd26e118182566b5194fb87de535e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.2 MB (19206388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0002a70187f7b872f3bb219e34f8fb015ac81f9d4d23fffd020ec4a1e1189b67`
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
# Tue, 09 Dec 2025 23:15:46 GMT
ENV NJS_VERSION=0.9.4
# Tue, 09 Dec 2025 23:15:46 GMT
ENV NJS_RELEASE=1
# Tue, 09 Dec 2025 23:15:46 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
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
	-	`sha256:07154c2ec8bf7f956bb2c650781cdd3ba12137ec92cbe3ec4d25c225df6c50b3`  
		Last Modified: Tue, 09 Dec 2025 23:16:00 GMT  
		Size: 14.2 MB (14240316 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:900be1298b7e3ea07f2e152be24bee756d8f576f67d149ea467d6a155cac47c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.9 KB (904910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd9be894354c6f5c7e5862a1ed4e1b94f1eedbeabecc732663f4dc03ba7e8d7f`

```dockerfile
```

-	Layers:
	-	`sha256:148f23549fe53f365eda0bc6ebf09b2f7e810a8216eb4df29e3a4c9de502c995`  
		Last Modified: Wed, 10 Dec 2025 00:51:20 GMT  
		Size: 883.7 KB (883683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd8f7bc65023135a47aa97afef1f4b25ac17a9fae0177e6707c2b8c13cfe2505`  
		Last Modified: Wed, 10 Dec 2025 00:51:21 GMT  
		Size: 21.2 KB (21227 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:f89b7511c1ceb783d4978f4ec64ab5d9dc7cbed484847a76fa55feea09a5f00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.0 MB (22972004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10afed3caf3eed1b711b8fa0a9600a7b488a45653a15a598a47ac570c1204cc4`
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
# Tue, 09 Dec 2025 23:10:40 GMT
ENV NJS_VERSION=0.9.4
# Tue, 09 Dec 2025 23:10:40 GMT
ENV NJS_RELEASE=1
# Tue, 09 Dec 2025 23:10:40 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
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
	-	`sha256:9afea992cb633e8b6280d56efc719c23323eee893368363b3c9d2d28bca323f9`  
		Last Modified: Tue, 09 Dec 2025 23:10:54 GMT  
		Size: 16.9 MB (16899374 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:085d03f5cf0520473d5719f4d33aa30846c7b22c2173b867ef2febb252f6a7ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.0 KB (905002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3973d20830e0bada537b1c2371505ad0de2fa51ef4638286948a3418d9c110`

```dockerfile
```

-	Layers:
	-	`sha256:81eecc9295df1574e396d5c73aac10c776fed39c956b1c9da4d1defabbc2b258`  
		Last Modified: Wed, 10 Dec 2025 00:51:30 GMT  
		Size: 883.7 KB (883727 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1779b8a5a13f13743929094c5406cb1513dca8b644986f90d13f91c05ec7fe1`  
		Last Modified: Wed, 10 Dec 2025 00:51:30 GMT  
		Size: 21.3 KB (21275 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine` - linux; 386

```console
$ docker pull nginx@sha256:1922ef621ac5c21f713ae5915518d5a7ade430c9e19b757a27288108d2d1f182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22188190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebab851672ab734b89b6621a8ccf64b3ed2cbbb1721e68018a7fa9bc2702f162`
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
# Tue, 09 Dec 2025 23:14:57 GMT
ENV NJS_VERSION=0.9.4
# Tue, 09 Dec 2025 23:14:57 GMT
ENV NJS_RELEASE=1
# Tue, 09 Dec 2025 23:14:57 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
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
	-	`sha256:2c81182dc81bc8ea6b2cceae17d1f32e508943efb79918f3a8b930569a696e7c`  
		Last Modified: Tue, 09 Dec 2025 23:15:13 GMT  
		Size: 16.6 MB (16568219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:ad56766652e538c1eed7a70ded210a401ad0249d45f766c64460fbd5623454ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **905.2 KB (905231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c91a5b26d4d26c6bcbe142c499ec3be8b4774fa0f508aec844dd88d39140c2f3`

```dockerfile
```

-	Layers:
	-	`sha256:9fb249572b29a774bc5a9b95b4cd809be8cc4ab253176c33f894b26594667071`  
		Last Modified: Wed, 10 Dec 2025 00:51:34 GMT  
		Size: 884.2 KB (884194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c21bb19c23693cb0e26fec397c0768aa18a4ea63175bd8ad8128761ee5fed545`  
		Last Modified: Wed, 10 Dec 2025 00:51:34 GMT  
		Size: 21.0 KB (21037 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine` - linux; ppc64le

```console
$ docker pull nginx@sha256:c7744948e512281a0d7653fc4f746119824e09bb76958d0224af60cb1c7fc98c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23293575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a78f1cbe3f55ea3d4ed80054ef969c94cbfbdd9704c6dfb4303a8ad693a4dc8`
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
# Tue, 09 Dec 2025 23:12:31 GMT
ENV NJS_VERSION=0.9.4
# Tue, 09 Dec 2025 23:12:31 GMT
ENV NJS_RELEASE=1
# Tue, 09 Dec 2025 23:12:31 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
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
	-	`sha256:f37d93b0d71612e5ad644793a2c3d354204a38bd6d5828be8b3f868dc67be6ba`  
		Last Modified: Tue, 09 Dec 2025 23:13:08 GMT  
		Size: 17.5 MB (17514796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:47d9b69426504404f50c8fc44b49a8790db446acec80c9fc0e52a431378d2b1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.8 KB (904847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb08fa9bc21149d455fc4a55838600876d4576afb10066f1484d011de110978e`

```dockerfile
```

-	Layers:
	-	`sha256:7d132b8838d305b15f59cdb42dc8ff298084e727723fee9783265853e1a70ff5`  
		Last Modified: Wed, 10 Dec 2025 00:51:38 GMT  
		Size: 883.7 KB (883668 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:301a8f55811a88767eed8d61e9dcfcdbfc6e20fba74ccb21535f1d43922d10d0`  
		Last Modified: Wed, 10 Dec 2025 00:51:39 GMT  
		Size: 21.2 KB (21179 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine` - linux; riscv64

```console
$ docker pull nginx@sha256:12adff7a08fae07d12d7dbe89d3ee7f2586f679fa8cabea6fd3be33642aeded1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20649972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8555cc8a185222889ecec7b185d93582477a4c182a92c1c089a24a04befc9f1a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 03 Dec 2025 19:29:39 GMT
ADD alpine-minirootfs-3.23.0-riscv64.tar.gz / # buildkit
# Wed, 03 Dec 2025 19:29:39 GMT
CMD ["/bin/sh"]
# Wed, 10 Dec 2025 19:33:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 10 Dec 2025 19:33:24 GMT
ENV NGINX_VERSION=1.29.4
# Wed, 10 Dec 2025 19:33:24 GMT
ENV PKG_RELEASE=1
# Wed, 10 Dec 2025 19:33:24 GMT
ENV DYNPKG_RELEASE=1
# Wed, 10 Dec 2025 19:33:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:33:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 10 Dec 2025 19:33:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:33:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:33:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:33:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 10 Dec 2025 19:33:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 10 Dec 2025 19:33:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 10 Dec 2025 19:33:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 10 Dec 2025 19:33:24 GMT
CMD ["nginx" "-g" "daemon off;"]
# Sat, 13 Dec 2025 22:11:44 GMT
ENV NJS_VERSION=0.9.4
# Sat, 13 Dec 2025 22:11:44 GMT
ENV NJS_RELEASE=1
# Sat, 13 Dec 2025 22:11:44 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:9929557817a4c85b33d6dbeb491f7396ef32added7e77de7ac1b644ed0975313`  
		Last Modified: Wed, 03 Dec 2025 19:30:17 GMT  
		Size: 3.6 MB (3583519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f5dc30ca4cae7d90d25cffca2865649700c213bd886f0eafb1014381ed85787`  
		Last Modified: Wed, 10 Dec 2025 19:34:04 GMT  
		Size: 1.9 MB (1898678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4806dba53da4c85a7804ed3404e12cbdcd7b6cfcb71a7308cd2daca34631b06`  
		Last Modified: Wed, 10 Dec 2025 19:34:04 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1e880db5f8f85550e7cd7081e9511eabb82dc56ad87d9de82ea5b6a4b7fcff9`  
		Last Modified: Wed, 10 Dec 2025 19:34:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d8a82e2113064c1ba089baf8654a38068d5950ef3f1be0ae669c6d6dcd3937`  
		Last Modified: Wed, 10 Dec 2025 19:34:04 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cd42e232ea2740a0d1d3781be12bd98ee64c6be30c7ad312fa221fc0120b733`  
		Last Modified: Wed, 10 Dec 2025 19:34:04 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7fc3afc7ce9361d0800db9744ac89d42e453844375bb6d3f773805b13e8c620`  
		Last Modified: Wed, 10 Dec 2025 19:34:04 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e985e4508aa2d55d9b7698c6852fc5562d9e6b1b521fb24c4a350546615d9694`  
		Last Modified: Sat, 13 Dec 2025 22:12:36 GMT  
		Size: 15.2 MB (15163172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:7c51382c4e4b4f3bbd7425b5b10006f2541e9376f83a0a38e86b642c5454ffdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.8 KB (904843 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c845662c71d6368bb498e020e89376807fe6d409c7e502b50be60e2959053874`

```dockerfile
```

-	Layers:
	-	`sha256:5f933ee56e99134ad136d51b094235e17456a2cacdca95bed777b4d3c76402c6`  
		Last Modified: Sun, 14 Dec 2025 00:50:34 GMT  
		Size: 883.7 KB (883664 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73eebcb9a571f5371d277154b01614e49b2b62676125cf42588527458e761b3d`  
		Last Modified: Sun, 14 Dec 2025 00:50:35 GMT  
		Size: 21.2 KB (21179 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine` - linux; s390x

```console
$ docker pull nginx@sha256:cd2674bee56c058e7adad8b80eb09d86bf9d702fc69bcf8ce714c971c55e71f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23061599 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56af174fb0de036f5cc0cdcb2186b13eb8731a9d39142034944d06abd6ffeca2`
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
# Tue, 09 Dec 2025 23:12:02 GMT
ENV NJS_VERSION=0.9.4
# Tue, 09 Dec 2025 23:12:02 GMT
ENV NJS_RELEASE=1
# Tue, 09 Dec 2025 23:12:02 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
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
	-	`sha256:4bd7b5c357a712d580d2725da5b71cdafa80bd8351ad353c077944dc5b220d60`  
		Last Modified: Tue, 09 Dec 2025 23:12:20 GMT  
		Size: 17.4 MB (17360634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:942c404b4deb22d69f21201bc2dd31f8ecb22f3c71b0ed854957af6e66b7fa27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **904.7 KB (904697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:440ac141ddf2423039cdbaf17339582489f82ee8ffce7ceeefcbb8c7d0f72497`

```dockerfile
```

-	Layers:
	-	`sha256:524be11c554a69e677da7197a3096c30c51880530d57a1504dfb7b6e99a737e2`  
		Last Modified: Wed, 10 Dec 2025 00:51:45 GMT  
		Size: 883.6 KB (883598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f90b7569d5d9ba42c74527effc61a00652c6018c374c2abce21f6e02d0c9c5a6`  
		Last Modified: Wed, 10 Dec 2025 00:51:45 GMT  
		Size: 21.1 KB (21099 bytes)  
		MIME: application/vnd.in-toto+json
