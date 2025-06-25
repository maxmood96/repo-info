## `nginx:mainline-alpine3.22-slim`

```console
$ docker pull nginx@sha256:e4e764cb35f666f44dd4e1da4291a5f73bb8bff2a9464ccecd8a05a2b7226ad5
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

### `nginx:mainline-alpine3.22-slim` - linux; amd64

```console
$ docker pull nginx@sha256:6ae2b2a9136e5d5eea755176e4faff6d4a864ff44ffd4a0dbf7db3006c67de03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5611106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e70c510cafd798116fe32781158d6e5ff54f19287713c9370654afd4342492a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86_64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:fe07684b16b82247c3539ed86a65ff37a76138ec25d380bd80c869a1a4c73236`  
		Last Modified: Tue, 03 Jun 2025 13:30:12 GMT  
		Size: 3.8 MB (3796846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7062d09e028c442f2b05e76286341d9b23a69a42b9ecd3d226911a5200bc86`  
		Last Modified: Tue, 24 Jun 2025 21:26:15 GMT  
		Size: 1.8 MB (1809667 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb746e72516f99f0b4f5204c47f8c2aa325a4a9d075769800c42548fe722b25d`  
		Last Modified: Tue, 24 Jun 2025 21:26:15 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ff9baf1741d1f2a4a5df1b44b2f09931318cb1a9201f23a01cb295e0274768`  
		Last Modified: Tue, 24 Jun 2025 21:26:15 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c127093dfc748d5aae28bdf3d96936deb033e69cb643eeb75d6070e4333f7c4`  
		Last Modified: Tue, 24 Jun 2025 21:26:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63dda2adf85bd92ed611cda1b94324396aefe5afe0b7b39a72b4ea6362c40552`  
		Last Modified: Tue, 24 Jun 2025 21:26:16 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55ed7d7b2def46fd4870c4bb5743ffd31dae1da58ffd897893978b789c62943`  
		Last Modified: Tue, 24 Jun 2025 21:26:17 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.22-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:939abb131ba14b8505ed45177c4fc4159a825924acb952afb0be11f92c00cdbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.2 KB (504201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6208d0af768784938592b657fcbfeca5af7acc746e2310f305cc6741f2f194ad`

```dockerfile
```

-	Layers:
	-	`sha256:1b71956eb0c006297fcfdbaf56f61182f9ea4f53b98f81f20d69a87489ad927e`  
		Last Modified: Tue, 24 Jun 2025 23:51:40 GMT  
		Size: 475.3 KB (475291 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b201cfa08fc1ad4a15b14e96335965a2071aa08186ca3df09fac44a7e86784`  
		Last Modified: Tue, 24 Jun 2025 23:51:41 GMT  
		Size: 28.9 KB (28910 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.22-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:c52b0734c5ad7eaa655c9f4f4258caf088f881fcf42c5db3358cdf7558ff1b34
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5309339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c58e51f7bea839b4b0e8ceac8df3d296943c07e6771a9c46b374ad0642449db5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armhf.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5ddfb4a71b19e6dcd52b9c46193b6249cf9b39300f0f664f0d682463a4d48e6c`  
		Last Modified: Tue, 03 Jun 2025 13:30:27 GMT  
		Size: 3.5 MB (3500929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37982501c774100008078686b1c2dfecd7d17d8066db30aa0987d509ab2e7b89`  
		Last Modified: Tue, 24 Jun 2025 21:26:24 GMT  
		Size: 1.8 MB (1803812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44e649c8145fe95c34d3c43cc123faa4c05d80342bf0063ecc67053c83ebdbc`  
		Last Modified: Tue, 24 Jun 2025 21:26:24 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b2cb614bee807118921d6a296c61c534faf8a8fdd2383dbf12c45d3bbf05117`  
		Last Modified: Tue, 24 Jun 2025 21:26:24 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c416415689dba1210973cedfa8d3bbec15390b036526b8409f8ae45f6544ef`  
		Last Modified: Tue, 24 Jun 2025 21:26:24 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00573dbc76eba19e6ebcbf5207a020e4739aed93004c1b3325dd3ffb8a6ced2`  
		Last Modified: Tue, 24 Jun 2025 21:26:24 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:007fd22900a1fe1df564b92b43c06995e652d8f222dc5c275f8dff2058c9c06d`  
		Last Modified: Tue, 24 Jun 2025 21:26:25 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.22-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:832d6a53c5d53b333d0e93dea501b6af44ab055bdab8597dd1e5aaf5acdda1cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.8 KB (28819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d54649bd1b16df0d4798f7c9e8132ec56001730a6af148d5eabf0c6202d426f`

```dockerfile
```

-	Layers:
	-	`sha256:287bdbbc119543ecb8ee25f805207a58ba16072c220ccc04bfef17b231602f12`  
		Last Modified: Tue, 24 Jun 2025 23:51:46 GMT  
		Size: 28.8 KB (28819 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.22-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:a1f0441867766f5f860129338d7450b4bdeaef927881e181ed2574e3547a10c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.9 MB (4862676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23c4988e7ac92373938fdaf16be79cd05f5c18ad565b0f974783867d8502d4f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-armv7.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:22e4d17029cf647ff505d5389be90006efc5ed4178aed9a6d798a2bf7a675fc9`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 3.2 MB (3219181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e567e72bc040a78f5e20eaeff25ea60c41b2cf48d9c7b84d589c88fac86d80b`  
		Last Modified: Tue, 24 Jun 2025 21:31:58 GMT  
		Size: 1.6 MB (1638901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:603e69cfdc6510ceecc1046830cc76fd995ee6a15826e216a2459adda8c73ef6`  
		Last Modified: Tue, 24 Jun 2025 21:31:58 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e0b163fad28cbfbd7a282b6a2093ce7f1592449e7237c7f9d3496035ff76234`  
		Last Modified: Tue, 24 Jun 2025 21:31:59 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cefc3080f3d6a067cbfd344058114cafffdaa79e900019c3ae46080bd8271999`  
		Last Modified: Tue, 24 Jun 2025 21:31:59 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4696cc0f6f73fd16ac791c43b35dc619b330bdadc81e8d88d1f2ce01cdb39435`  
		Last Modified: Tue, 24 Jun 2025 21:31:59 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f095944e3d96c849a7009a945cc110a20cdfaed0aa6f67e5d2112bbfde693f89`  
		Last Modified: Tue, 24 Jun 2025 21:31:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.22-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:aef40818c7c5ea4e76dfb2f39aeca2110914df546b8ea33f6f022afa83856f07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.4 KB (504409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdc4a92c31eacf4c674266cb19d75ec36fb29ec72ac14c6879f8de7e3e2176f`

```dockerfile
```

-	Layers:
	-	`sha256:edf5b44d117df19e50cd6c573397490db9266664d9485593a8b70704526ad151`  
		Last Modified: Tue, 24 Jun 2025 23:51:50 GMT  
		Size: 475.4 KB (475375 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a45815bb42dd56b11be920395b8247b97fc9a1ce71448dd2ca226aa357ad6981`  
		Last Modified: Tue, 24 Jun 2025 23:51:50 GMT  
		Size: 29.0 KB (29034 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.22-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:380f760e8f2f1cb1114fa1f69d2572e210951d870adc3fbe46afb47737715d0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5942788 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcdeeab52fc3782f94a343d94e323a0cb61017757d6b24f0555317786942e5bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-aarch64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d69d4d41cfe2ee680d6972795e2a1eb9e4dc4ec3b3c5e0797c9ab43bb3726fa7`  
		Last Modified: Tue, 03 Jun 2025 13:30:13 GMT  
		Size: 4.1 MB (4135941 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d795a661d598f9be4b53a85553d9b23cd810889ff19e3c8a091df8047e96d69`  
		Last Modified: Tue, 24 Jun 2025 21:26:38 GMT  
		Size: 1.8 MB (1802260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57cda1772fb11bbbbebff43a544d9528eec9efb3aa448fa42ab119fd1db14a3c`  
		Last Modified: Tue, 24 Jun 2025 21:26:38 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b57be73a166a34ea30d0e832e9a4a886964aafaae61105b702847a28b88eeffc`  
		Last Modified: Tue, 24 Jun 2025 21:26:38 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbd194a4692986dc058e1b0ba45012cc40f638b32cd3246e1130cfa350cee8c4`  
		Last Modified: Tue, 24 Jun 2025 21:26:39 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a76d74c6861c4770471859c2fa633d253d7f596f7a9ea4a819106170c56a4cb6`  
		Last Modified: Tue, 24 Jun 2025 21:26:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05133958970cdffbc2d3b54caeea92f5445b783ef0cd9ee61709f3b891b448b6`  
		Last Modified: Tue, 24 Jun 2025 21:26:39 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.22-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3a3822333f2fba5235e9003cbb0af8dd355ebbb58f545618a12706dddb5b8c61
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.5 KB (504505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ed274a89c5a81ae062c3dd4a265c95522152ac65de6ddff1a815ef9f3d147f0`

```dockerfile
```

-	Layers:
	-	`sha256:6f7f1847456337a697a903d09038fdb7e3e63b7c7b76e17766f44aa5dcd01545`  
		Last Modified: Tue, 24 Jun 2025 23:51:54 GMT  
		Size: 475.4 KB (475419 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0acedf707d6901a2beb587bb28f2c768e2f4c31abcbf2dd4a96080f8c4a50f7d`  
		Last Modified: Tue, 24 Jun 2025 23:51:55 GMT  
		Size: 29.1 KB (29086 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.22-slim` - linux; 386

```console
$ docker pull nginx@sha256:e80262314d449f100c1c010f76b50bcac17dc48be6cb177382ae63208c7c1461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5499126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b8356512e4d4da8b5b85ce21b819922265bc202526d279285b1721c0faa321c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-x86.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c787620501b746b3aa9ec021f3ddb0b707572b5c68e33d73be392b9c078a4993`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 3.6 MB (3616029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:feab75d70fc2401819260c9dc7c1494312eb3cf1655021508516b75ecaf543a6`  
		Last Modified: Tue, 24 Jun 2025 21:27:32 GMT  
		Size: 1.9 MB (1878491 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4abaca86fba81b734d41c7ca3089c6ad44f4c321ef5c535bf8a311be5f339b9a`  
		Last Modified: Tue, 24 Jun 2025 21:27:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2005bc5e20b31112b188645791dbb208e51e464f77385f0a2e354dd7002b800`  
		Last Modified: Tue, 24 Jun 2025 21:27:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b68e7e83bd728010940948cc7126606b964b1b0a4fdd3ff79683f4ac2fbb35f`  
		Last Modified: Tue, 24 Jun 2025 21:27:32 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ffe95640712438345900483e7a5c8359924122c4a3e704e1f4c0162fab922c9`  
		Last Modified: Tue, 24 Jun 2025 21:27:33 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f157e206514cde1dc234944225f4b10a6a670d462b9f0de819005454872478e9`  
		Last Modified: Tue, 24 Jun 2025 21:27:32 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.22-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:20c3998d1bb8ae544be1ef6cad70bc320c559211996700d174b655f9bd29c41a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **504.1 KB (504084 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586ee12140cb84410ca4ba3303af2e6dd8766e72d34d304e14cd4312b9a14a8f`

```dockerfile
```

-	Layers:
	-	`sha256:ec489324c1305498991599014cd93135dc65e17e2ddf846f3a51f8836fbd2ae4`  
		Last Modified: Tue, 24 Jun 2025 23:51:58 GMT  
		Size: 475.2 KB (475236 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d85a158134bae5ce72ec1e09a70b467738b11accccf22eff8136bb9f328139e9`  
		Last Modified: Tue, 24 Jun 2025 23:51:59 GMT  
		Size: 28.8 KB (28848 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.22-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:9c335c0ada23cb70c1e5378085d532808e4eb5ba69c5eaff7f056bb2e8b59199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f18807a8f760ad6809ced2b5065562d3bf3b4f9e574e0ed63ae2db669802487`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-ppc64le.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:33a2433d89df7e794d1655fce70d7031d8065c9798bdc2931f7c98fcc8d310d0`  
		Last Modified: Tue, 03 Jun 2025 13:30:33 GMT  
		Size: 3.7 MB (3730187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbf175b07c62dcc59bfeb9fcb67bfd794d56eec4ab5e866f1f4ddd71e1a8810`  
		Last Modified: Tue, 24 Jun 2025 21:34:16 GMT  
		Size: 1.9 MB (1869709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7004bbc29c487e34e49172efc09f44e89a92a01d0ea22bd0d1d0a3daa8b143`  
		Last Modified: Tue, 24 Jun 2025 21:34:16 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f96751fbf1e7e48bfc280f262ed9c34037bf8464f6980aede2ac6f9c519ba7d`  
		Last Modified: Tue, 24 Jun 2025 21:34:16 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e3b3c10b63dd86fa4d07c97e5b760f94eb0da053ac464ba972b74a43841a8c`  
		Last Modified: Tue, 24 Jun 2025 21:34:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37dae07cc5499f9d79897f3519be0366967aa120212f384a1750d56bebc853c8`  
		Last Modified: Tue, 24 Jun 2025 21:34:17 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df3879ac94cb3a935a61f92c60090079b3c2a601ca948a8900f53cccf23904ef`  
		Last Modified: Tue, 24 Jun 2025 21:42:53 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.22-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:947527ba0009f2b44ce404a5889bfb109d324b165026651298c2f66b693435f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44ce8fd811698cf5def9c28f2a6f7ad0807255e840e1a8d31a2d1af95784a92a`

```dockerfile
```

-	Layers:
	-	`sha256:75827a9bfd41329c54fc0ae1cefb67047f46354e08dd2bbe7d8f53636ab316b6`  
		Last Modified: Tue, 24 Jun 2025 23:52:13 GMT  
		Size: 473.4 KB (473410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67fe33a01d6b3df23cd9113cdb637563dd97359e0c59da5aee7ca312757b7be4`  
		Last Modified: Tue, 24 Jun 2025 23:52:13 GMT  
		Size: 29.0 KB (28990 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.22-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:4e26e6a2355620f63513b7dbbb56a3f9825c20ed98368bf864b138acfef62fda
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5367320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:458d4887ceeacc8ad71f6723538f3a393ccf98850292ccba863ce898605de08f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-riscv64.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a0a4beaa1960bba353066d674aa0e3378b856b09e6d3f704d1755daa5d6c1d39`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.5 MB (3513811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1a63104c2b36021c6933e6b2683b1f9c51c8ba272247db4027ec43b7504c3c`  
		Last Modified: Tue, 24 Jun 2025 21:51:05 GMT  
		Size: 1.8 MB (1848909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db9f71c7078aacff58f0463b0893b6257fd8bf7e06d5079006fecd227dadf493`  
		Last Modified: Tue, 24 Jun 2025 21:51:04 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dad59f56bd1c55c9f823b8d5cea94db2b65d0c1740d089c7f71d2e41a15673c`  
		Last Modified: Tue, 24 Jun 2025 21:51:04 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f324311c20de14b2f0e3db74652d78170e1507382a97bb00a14753f0b2d4778`  
		Last Modified: Tue, 24 Jun 2025 21:51:05 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d37ef7fd3035f7fdab4a84a3dcbd741652d3b36026b789284c37c1ed5bbc1676`  
		Last Modified: Tue, 24 Jun 2025 21:51:04 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd7dcd4385f1484957e59b93a1f0dcb6c0849c964905ceee1a1e3982e2c0446d`  
		Last Modified: Tue, 24 Jun 2025 21:51:05 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.22-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:fa8fe123fcd4a647346a36f86e575a23c974930705aa682f9621af13176ce023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.4 KB (502396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e381d59b5f31ae3f64b23d330dfe31cae77fe9b9bc741d01687951ac09fbb25`

```dockerfile
```

-	Layers:
	-	`sha256:16bd04e1d55fd3347d175e088d9de3c3dec763d1d6fded137e785ffd1946af76`  
		Last Modified: Tue, 24 Jun 2025 23:52:17 GMT  
		Size: 473.4 KB (473406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80d61f0f2b6b330f8afb74bd423459e983924e8af95e95dec17e80e79024c826`  
		Last Modified: Tue, 24 Jun 2025 23:52:18 GMT  
		Size: 29.0 KB (28990 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine3.22-slim` - linux; s390x

```console
$ docker pull nginx@sha256:f022fc3fddf404b18f72e742f4a113fbfa228df8a4ae8742993dc5e530667303
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5561907 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06738b838df5a72559fa14f8aaa27b42a2775a0be441b7662acb669422188ae1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 30 May 2025 16:20:41 GMT
ADD alpine-minirootfs-3.22.0-s390x.tar.gz / # buildkit
# Fri, 30 May 2025 16:20:41 GMT
CMD ["/bin/sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Jun 2025 20:52:14 GMT
ENV NGINX_VERSION=1.29.0
# Tue, 24 Jun 2025 20:52:14 GMT
ENV PKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
ENV DYNPKG_RELEASE=1
# Tue, 24 Jun 2025 20:52:14 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"400593da45fc0195a01138c0c23a06059da1c6a2e26959f2c4c95fbaf63436ff211665ef01392d2b775a0133d5b57680dabe51b840a55f82e89621e84cf651d1 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Jun 2025 20:52:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Jun 2025 20:52:14 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Jun 2025 20:52:14 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Jun 2025 20:52:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:47a70fdc8ac4c1273de626dc7710d3e19cfd5b9f3e10cfc4b14602bdfffbffe1`  
		Last Modified: Tue, 03 Jun 2025 13:30:43 GMT  
		Size: 3.6 MB (3647529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2af16ee26645af91cb40377d08a9ac0f9a1b781e203027fc014c439273722e56`  
		Last Modified: Tue, 24 Jun 2025 21:31:56 GMT  
		Size: 1.9 MB (1909781 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2de4e1da3b907d3682844ac096e3ac5d4eee1995403b1c71a000493ed4cfc030`  
		Last Modified: Tue, 24 Jun 2025 21:31:56 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6c3c494fbf75933bbdfeae52105a1a9526daad66db0b43b8150764f3c25cf58`  
		Last Modified: Tue, 24 Jun 2025 21:31:57 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d02acb427362d535f9670ec20611e8eb6a8e615136a8e74c1e63340cc18c414`  
		Last Modified: Tue, 24 Jun 2025 21:31:57 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8935ba04b3780c7259ee729dc55f830fccc5526127f03f22d803a575773360b4`  
		Last Modified: Tue, 24 Jun 2025 21:31:58 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3790b81704800c76e719f72ac6030f9785d0830e67bdf7cecdfbe6f36ded766`  
		Last Modified: Tue, 24 Jun 2025 21:31:58 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine3.22-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:69861e101c9d1cd4a5a32f10cf4a457eb06136989f8a97eaa5636afc0965fe74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **502.2 KB (502250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19b8e9d9446d08ab4252023576d6b7af13410ec81ca2de856392651b0615fa6e`

```dockerfile
```

-	Layers:
	-	`sha256:dc9da83ac8ad94808a1bfce5957bb3666608066bbfbbfee59fc611defd876a63`  
		Last Modified: Tue, 24 Jun 2025 23:52:21 GMT  
		Size: 473.3 KB (473340 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8609b51ded354bc747eb479da581d55a56a86f92ad50fedc219b97aeac7a2e2c`  
		Last Modified: Tue, 24 Jun 2025 23:52:21 GMT  
		Size: 28.9 KB (28910 bytes)  
		MIME: application/vnd.in-toto+json
