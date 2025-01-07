## `nginx:mainline-alpine-slim`

```console
$ docker pull nginx@sha256:e9d4fe3e963d75580048fa9a860c514312c328f536595022e597d1c4729f073a
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

### `nginx:mainline-alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:a2d509cbd8a5a54c894cf518e94739f0936189631a24d05bb7c90e73ec639251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7684638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65e3b14358d169d117e5462344c62ef50181b6ef0af0050954900db8d5b4540b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10e486de1ab216956a771c782ef1adabef10b1bfd9a3765e14f79484784e9cd`  
		Last Modified: Tue, 26 Nov 2024 20:23:14 GMT  
		Size: 4.1 MB (4056137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af9c0e53c5a430c700d068066f35cb313945c9917bee94108bae13a933f6b6b4`  
		Last Modified: Tue, 26 Nov 2024 20:23:14 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2eb2b8af93a0c4d2b5f5a70ed620869b406658462aba70b03f12f442aa40cc1`  
		Last Modified: Tue, 26 Nov 2024 20:23:14 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e351ee5ec3d4f55b4e3fce972c2a34a5632ede02602dfbcad85afc539b486131`  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbbf7d28be71101773e4440c75dbbe7ed12767763fbb2e9c85a32a31f611169a`  
		Last Modified: Tue, 26 Nov 2024 20:23:15 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471412c08d15ee3b0c86b86fe91a6dd0e17d1f4d1b6d83a7f68e9b709328bf3d`  
		Last Modified: Tue, 26 Nov 2024 20:23:15 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c4e61d4d1deb21447238790672ca1acc370ccec8ce94ab2908b181712ae35cd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.9 KB (495919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b071008302fccc542583f807bd911ac72198d0084b2709d62b862aa71ded885`

```dockerfile
```

-	Layers:
	-	`sha256:dbca25511a2f0b5c1949f101201bcb4f6858cb3415bf39ddca63cd840122124a`  
		Last Modified: Tue, 26 Nov 2024 20:23:14 GMT  
		Size: 465.1 KB (465148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:35bbec47f8de16becd8c391483d2034367cfe7c16b938cd11e6a2a1e58f42cdd`  
		Last Modified: Tue, 26 Nov 2024 20:23:14 GMT  
		Size: 30.8 KB (30771 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:8551258c172e1c470831dde797c361ba30f8c078748869cad1a1826bffe5d2a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7228136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6460efbb556bbebdb46f8f3fd4e896fc1609ff5594c40fe77ebf3b7d2dc11abb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5aba61ee2b140616059b7b32883cb6722e498b13665a43e2bd0f80f9b390bc3f`  
		Last Modified: Tue, 26 Nov 2024 21:08:09 GMT  
		Size: 3.9 MB (3856940 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b14a4b656660123da1b3fc20b091800c512a033de7a42dcdd955500dc9d74c7`  
		Last Modified: Tue, 26 Nov 2024 21:08:08 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1d32d0076c05b651b3a9167e3694055e5387601c11a650e0fba0967accf755`  
		Last Modified: Tue, 26 Nov 2024 21:08:08 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37509b8108e228331eeec22e7263d08d87f6b9766cc3b9448f893ed7cb315083`  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63da2f59bf96b515fccb075194ce683548d1efa7ad2835bd1bd2e8be7f15c2ec`  
		Last Modified: Tue, 26 Nov 2024 21:08:09 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98c94687a5de3597655766fa52e0ee7f048fcb1aa251c1e1c87ff12c4d242bab`  
		Last Modified: Tue, 26 Nov 2024 21:08:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:967da45c1b35f49afbfa5afa2abc6711e45fc2e6ab7405bb43522bcfdbb3ee7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bb6ff9c5ded0eb8de6369804bd167efe7e544e2d719628f19cf13b33829de4f`

```dockerfile
```

-	Layers:
	-	`sha256:01708ccb92217c7781e2a6036d3b41e19d60f7f7dbcefeacb4b81dc5c88b8e83`  
		Last Modified: Tue, 26 Nov 2024 21:08:08 GMT  
		Size: 30.7 KB (30680 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:600a5af9a8d7f93121559f6598e674419feefd32e67354fdcf636c7096f7c227
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6641793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35f27234709f40f07af2363aca093662d34d186a4efb033969ee745abce2d2e1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da25195ddb822acf37d57ea78d0dadbc196377386efcfda0173becc62e589e59`  
		Last Modified: Tue, 26 Nov 2024 20:28:57 GMT  
		Size: 3.5 MB (3541707 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88c4498e22eb2059cadfb46a32a087788a647690496d30bd8a31924212630025`  
		Last Modified: Tue, 26 Nov 2024 20:28:57 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7236c453c4166657f5b84ac92411299e7aecca6e20e4d5d4a4fb721ed51a8f24`  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a769eb2f10d6bc3d4539e28f02cc7ea6ccbe1d6e568d76dbaad9bb7d36271a82`  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e7ab3e878a19e73ef962156201c89b08c1cbf35f5cf009f1358fce7c522141b`  
		Last Modified: Tue, 26 Nov 2024 20:28:57 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b70af03f12e72139000fb97f455de11977a7bf1b1ac75645b5882decb03b6ef2`  
		Last Modified: Tue, 26 Nov 2024 20:28:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:783275f1eb7319a1b3d24cfc2ff3ef4342b9ac69c525b6dc4e5a6e48befdaeb7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.1 KB (496127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8fcac2d9df9bec65d18270315315ffb74933e7609420f86e95c2d821fe1ad87`

```dockerfile
```

-	Layers:
	-	`sha256:2a61c04bd67ad8ea6baebdb1617b46cc9bcf20dd2254f445fe81de1ea565248e`  
		Last Modified: Tue, 26 Nov 2024 20:28:57 GMT  
		Size: 465.2 KB (465232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6dbd3491ba12174aee87f26c440ceda08ebd519b8bb465b54035eaa4f63ca3d3`  
		Size: 30.9 KB (30895 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:abe5bc2cf13c05a181c5fa6ef04d4ca04812d00d52528c2f7714d3c6151b2ed4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8596193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d835eebde567067ed225505b27a739f489bd723185fb3174ed093a7f981d1e91`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb15b755ebd8bc952bebaeaa06146588eb251b581cb9f1ee854686de2130a2d`  
		Last Modified: Tue, 26 Nov 2024 20:23:54 GMT  
		Size: 4.5 MB (4503872 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f4e4c7e275af8dd7fedd5c2194d287eb609435973ef29f1c4f5526d105a67e1`  
		Last Modified: Tue, 26 Nov 2024 20:23:54 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f25994e8065c49a45802ba5b3eee92fd5796b0d06f716818685582eba26157b`  
		Last Modified: Tue, 26 Nov 2024 20:23:54 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d54cacdeff19a98ab91fdabf2f43ea9ac82cfe558bcf1f681acfcfed41a34337`  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d10f0cbc450c8fb604b147325b56374ec05a7e4de914afd7eaf428be419cdb3`  
		Last Modified: Tue, 26 Nov 2024 20:23:55 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dad217f69471ed9c57eae3c709f0ae670346cd438bcebbdf6050c5deb431f7`  
		Last Modified: Tue, 26 Nov 2024 20:23:55 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:f3695083c769e3b6a1497e1a78f9dce932050cc4f45a3b4875e1aee212a3c78c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.2 KB (496223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b05956c0bbc837cf20ca0502ae632dd85f621b1478d7685f1a45a77e35ec459f`

```dockerfile
```

-	Layers:
	-	`sha256:7938f81c9a4b08ef9b7078b190ddbaf79a5e7d84252db8ce85180d936b4c7917`  
		Last Modified: Tue, 26 Nov 2024 20:23:54 GMT  
		Size: 465.3 KB (465276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:feed14a6554eed219d8baaea85ed7749b3aacd321e85b0a784c3f39b00f979fa`  
		Last Modified: Tue, 26 Nov 2024 20:23:54 GMT  
		Size: 30.9 KB (30947 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:8c210ecaa33b122577ffe9611957bb2b53ad13cfa387adb25c6b195b151eb474
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7570356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1469a1878d1fe57d8ddf28febbce283aef1f6497bc770d806e6d7217249668fc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36c77a5adda0ac1cb797a3981cf47fba63e38be9937eddc33264d4700b7f85e4`  
		Last Modified: Tue, 26 Nov 2024 20:24:48 GMT  
		Size: 4.1 MB (4096548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9acde86dcc25b5c43c89d099cb22f9df9f48558ff7465baf1aad50692974e2a8`  
		Last Modified: Tue, 26 Nov 2024 20:24:47 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f947748ab311c2b35e25d224ddaf1d4dcfd86343a1f5ae6a7ce943459db5e144`  
		Last Modified: Tue, 26 Nov 2024 20:24:47 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eccf6569cfc3ccd961ac9ced9863752a4f3e65efe6290b0bb0abd65a45237a38`  
		Last Modified: Tue, 26 Nov 2024 20:24:48 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a4ba2d08271aa8c2a991a14acceb0a724e19a83d324e78ea5864d3e6b9cd7c`  
		Last Modified: Tue, 26 Nov 2024 20:24:48 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4bbb83b5c8500eea8db517c1b6c46d08c92445d1397130506b0685e72e45ac`  
		Last Modified: Tue, 26 Nov 2024 20:24:48 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:497ad1fd492d493c510ea6c5b0710324f8f6c48982f6c9c1246c76b9ee5085da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 KB (495803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3a83f1336f05fec9f469421df982e8003368cd90c32c79f9db990cce2893631`

```dockerfile
```

-	Layers:
	-	`sha256:2b8cdcbb5edf804aeacd93d5d75fd091ec5ee6a9f0fd0d8481e387bea62b411b`  
		Last Modified: Tue, 26 Nov 2024 20:24:48 GMT  
		Size: 465.1 KB (465093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:05a10246a53fc3aec5879d95e2c1251ee3d4231f76c5ae5942c5feccb3381981`  
		Last Modified: Tue, 26 Nov 2024 20:24:47 GMT  
		Size: 30.7 KB (30710 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:6573907a2512b08814f9ef68a8f4d040bcbeb5e621743d2976a0c1ba2b851f9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7693496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b4dcdd370b408f2d402b7b00d7238b937815ce2e21e93d659e5cd3b3098e19a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2310588c7b1695223a0510c55ff892f5f9a1d4c2aa7f884fb585802ed53ecf7`  
		Last Modified: Tue, 26 Nov 2024 20:31:57 GMT  
		Size: 4.1 MB (4116433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d51ce234cc7e9db2fffa70497f31417059dbc8916fce3f1b68b7ed856f984e4`  
		Last Modified: Tue, 26 Nov 2024 20:31:56 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:404ead9e77402ba623da5cce2825f426834d5c1ee9de6b02635f9f3142a8d411`  
		Last Modified: Tue, 26 Nov 2024 20:31:56 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c45fcdfa27a38d357e49ac70d8149533ffb1e5d9eee55b9d65e72562241419f`  
		Last Modified: Tue, 26 Nov 2024 20:31:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64d0c3bed69fed170992cda69555c05e5f15310c3851727ea3a23356b9e1f6ba`  
		Last Modified: Tue, 26 Nov 2024 20:31:57 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a2c184e8f847a6f06bb88fbcd245621aa3b88994b05112d1e0291505879fec9`  
		Last Modified: Tue, 26 Nov 2024 20:31:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:37d81191e024ce0a74d6ccd6e4e80c42054f87f024e80c19ab78459fcf3d5a41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.1 KB (494116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41bc067cfcf9e356c679828bf19339f90d9ce3ae9dc343f06af2c58c86f2f950`

```dockerfile
```

-	Layers:
	-	`sha256:9fc90b0f202d945a4bd5d092981b28241e34be162db6c8734577c1ff00b0305f`  
		Size: 463.3 KB (463264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13e364bdecb10528685ece3d33e7b1e9f5e5d73cce341f8a7ab470cfc35238d0`  
		Last Modified: Tue, 26 Nov 2024 20:31:56 GMT  
		Size: 30.9 KB (30852 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:67e77c0b841b8e62ab7ee093bf6d65c2c1397b78038ffbeefbf1cdeddbd1b94f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7284100 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b8651eb7685cabe9d6952d4d0553d8e8e7dc9200a75c36e9a8bf8306b7a6643`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a504a3907d918e853d8ea55ca5e0c8cb7be9cba8d560eb3f1cb8eb9775940a5b`  
		Last Modified: Tue, 03 Dec 2024 02:07:25 GMT  
		Size: 3.9 MB (3908016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4781d7782d2bcb5f50d1e005e2d28082a40317306252cc9392818f5fee074d1`  
		Last Modified: Tue, 03 Dec 2024 02:07:24 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9189ab81c4802b0314eb2fca96e84afc6ab8e9df82c9e3e0fcf5b10ef260a296`  
		Last Modified: Tue, 03 Dec 2024 02:07:24 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:212efe735a1f62deb7f2b4de11c98460ddfc01ae6d00e4afedb5ebb959267fce`  
		Last Modified: Tue, 03 Dec 2024 02:07:24 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:360f78832f82dafb51ce155aa772c00f1e0d35907a2354fa051e390b41a2cd5c`  
		Last Modified: Tue, 03 Dec 2024 02:07:25 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec32a08d306d489afcc6441b8587f13f41d82f170346f1d48b9a8d263dfdb62`  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:d1e32a7807853d87633020db98deb20fe7ac84a967e9d8c966ece882f9a12f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.1 KB (494112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:45b38cb5b7bae0d78000eaf2193b146a82f0420120be90a44933d18275283b93`

```dockerfile
```

-	Layers:
	-	`sha256:1d1e1a228c4aa1573842e9e54d25d81fab1f087fbbdb3d38d3e846d194ee422b`  
		Last Modified: Tue, 03 Dec 2024 02:07:24 GMT  
		Size: 463.3 KB (463260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e7fd0c49d98736f9415fd6a30f73a9d8d55049b19e02e085d5581f008c46309`  
		Last Modified: Tue, 03 Dec 2024 02:07:24 GMT  
		Size: 30.9 KB (30852 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:90c019cddbfcd88a83192843dde8775776917c6e9748d8fec0f3c2d20db036e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7504459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b4b49b1296ec3d5a1a897b4283fe614135e7febbdc841c0ec4e114727de1ab0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 26 Nov 2024 18:42:08 GMT
ENV NGINX_VERSION=1.27.3
# Tue, 26 Nov 2024 18:42:08 GMT
ENV PKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
ENV DYNPKG_RELEASE=1
# Tue, 26 Nov 2024 18:42:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"5617feecfb441cd972b9ac51a2fd78384a3d2bde2f399163be0746d44ec8f7d8c47234af4f6b0012667c3d0446cced521f55f8f71254415e3766c2e3802bf960 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 26 Nov 2024 18:42:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 26 Nov 2024 18:42:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 26 Nov 2024 18:42:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65a6583ba918b1c7c23f7c3cd13a37d6cbf8e93e5c5c56bf50827b1e160a1a50`  
		Last Modified: Tue, 26 Nov 2024 20:31:07 GMT  
		Size: 4.0 MB (4038244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf5c518b7f42dfaa9660e010f5b71f80da05c111809b78b320bf52f6bc99902a`  
		Last Modified: Tue, 26 Nov 2024 20:31:06 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5674a7223983f5dc1cacbcb353d4c213805a14fe6f2303a230a7044ddf2ea0e0`  
		Last Modified: Tue, 26 Nov 2024 20:31:06 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ed63e46e92d1caf65710a1f32ae618b77d61e19fdf36a2f6dfc1702ed16730`  
		Last Modified: Tue, 26 Nov 2024 20:31:07 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346ec8ac2cc7aecc7b554e2c5b54b91308137b26ba0e0220a82079ffa86b503b`  
		Last Modified: Tue, 26 Nov 2024 20:31:07 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33f91cd98e3337fb98e448b56df8ec31e4257fb5cd771d59df0752f7f913d73c`  
		Last Modified: Tue, 26 Nov 2024 20:31:07 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:e05e2ebfeaacefc37ece7b6035a962afd8e53fb62e3ff33c12cecc20bc1c4ded
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.0 KB (493966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdf3c2ff795e897ab6f15e52e2b4ae5bc18fdedce176533fc25835c0c72a45af`

```dockerfile
```

-	Layers:
	-	`sha256:f863551c04ab54f47e44d1f90dc988cb6fb82f45a6d7891870d2a1c1084b0f79`  
		Last Modified: Tue, 26 Nov 2024 20:31:06 GMT  
		Size: 463.2 KB (463194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8fe1ac06f96a9f8a77650540f3a5706abb41a2233e5a12ff50aa6898b8bd2c`  
		Last Modified: Tue, 26 Nov 2024 20:31:07 GMT  
		Size: 30.8 KB (30772 bytes)  
		MIME: application/vnd.in-toto+json
