## `nginx:1-alpine3.20-slim`

```console
$ docker pull nginx@sha256:5a56ae385906c5b43ccc99379bce883aa93dc0556d7f705ba501d819925e8fa1
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

### `nginx:1-alpine3.20-slim` - linux; amd64

```console
$ docker pull nginx@sha256:ed24ad5d1c519fe33a9fc461e890a3d088a65ee960a58441287fdb7161a5724b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5409346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9765c8de364c43f64ea0543a466bc123dfdfea9091cc3b3ec4d8e7b91eaf14b5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
ADD alpine-minirootfs-3.20.5-x86_64.tar.gz / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
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
	-	`sha256:66a3d608f3fa52124f8463e9467f170c784abd549e8216aa45c6960b00b4b79b`  
		Last Modified: Tue, 14 Jan 2025 20:32:58 GMT  
		Size: 3.6 MB (3626260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58290db888fa6af2884ef0423f4968e17479e82804d125b4e9e7de5ee13d5a35`  
		Last Modified: Wed, 08 Jan 2025 18:00:03 GMT  
		Size: 1.8 MB (1778487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d777e0071f6faf34b4215b907c08927d0f9ab503df5d5eada0868e48c03e99a`  
		Last Modified: Wed, 08 Jan 2025 18:00:02 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcfe8732ee679051780db1b6d2ea76f946c4518047ead6b87efc4d65662bb8d`  
		Last Modified: Wed, 08 Jan 2025 18:00:02 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37d775ecfbb935921bc194da16ebb1f5c80e1152b184861bf9ac703d220bbd8e`  
		Last Modified: Wed, 08 Jan 2025 18:00:03 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0350d1fd4dd6324588387625d61066d21828c7e9ce9cc67f2b5f5e531dfc678`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4aa363b71aa73f854818db3c0b64093049973d63d526f7739fc715278ff243`  
		Last Modified: Tue, 14 Jan 2025 20:33:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:7d9d67664b1ca003202e6755fe75d905f4e5d6641c35b632330d38a51d96aea8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.1 KB (495114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:935af07a9e6cf195cb5791f52669ad6b53fe89ac0b400d020300871a6304fe92`

```dockerfile
```

-	Layers:
	-	`sha256:ba38bc73eb7ae39d697611334606dc6a1b7c4170ef938d709a7b4d462d804ef8`  
		Last Modified: Wed, 08 Jan 2025 18:00:03 GMT  
		Size: 464.3 KB (464342 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4118a17f3c740f769925e911c870444190a71d7d6da9416627c845da45c3eb4`  
		Last Modified: Wed, 08 Jan 2025 18:00:02 GMT  
		Size: 30.8 KB (30772 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.20-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:cb37f545131b8eb1ee9db749f112473704df4f06893b0d8ca8fd999c0fecf906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5289771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89d0e11c20b1bff35b93d6b49169175c47e59680a7fdafe4ab7ab00ba21e208c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
ADD alpine-minirootfs-3.20.5-armhf.tar.gz / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
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
	-	`sha256:27a1f2308f194d2c8cfe617a324e0078d055d65032c6c342eae11afb7a8d38c0`  
		Last Modified: Tue, 14 Jan 2025 20:34:27 GMT  
		Size: 3.4 MB (3371473 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1fa2ed1ba9173a99f1d1ced05260d071500d06ea43f4ca0648c7c331d226180`  
		Last Modified: Wed, 08 Jan 2025 18:44:36 GMT  
		Size: 1.9 MB (1913687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9abfba777ff485a267c45202c6652c43ec564929b7621b670eb6cc408fcacaf1`  
		Last Modified: Tue, 07 Jan 2025 03:59:12 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d140d746d8f6f2c8b3dc26ff59f8f7a5b26911704b76b129fb0c11fe287f6edd`  
		Last Modified: Wed, 08 Jan 2025 18:44:36 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:614a5c18aa6995f0277a562649f0f81c3969247ac84bfd0a8cacc42ce435f335`  
		Last Modified: Wed, 15 Jan 2025 02:01:56 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23ae4efab8fd59b991d4c7504adfd30158edf3124f9859f66bd4db916be46acc`  
		Last Modified: Wed, 15 Jan 2025 02:01:56 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3540c2ec33addc323faf6978b8e800f53b0ba878bd0a12d4d2cb1dfd1cff2eeb`  
		Last Modified: Wed, 15 Jan 2025 02:01:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:937e01e9779b3d82bd46be83da8a7e2f6cfbac84e493f368ca09253ac58cc589
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c9ae69b1d3c29af1a1c95f92ff1ad5f53caf283a132ee4148ce338815357f6`

```dockerfile
```

-	Layers:
	-	`sha256:a636a6bcb1a3b239e920ec67c51acefe3f960da4a2cd156b907a58cf2124f755`  
		Last Modified: Wed, 08 Jan 2025 18:44:36 GMT  
		Size: 30.7 KB (30679 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.20-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:f8aa92ffaacf0284f7bb305ac562049d86f5c66b2d01f626c94a45eea4b48034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4849423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d756b494c2393f29fb778af86f2fceaf700535627ba533c4a591684758dc4358`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
ADD alpine-minirootfs-3.20.5-armv7.tar.gz / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
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
	-	`sha256:c8a32ed454e751770c0976636b8d0d0fccc4f778a2dd26c428067d613be1a299`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 3.1 MB (3095514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3340ea215422fb1f079bc91d2e8e146d1b0a8220aa3596d9a2719dad8f008b6a`  
		Last Modified: Wed, 08 Jan 2025 18:46:15 GMT  
		Size: 1.7 MB (1749307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e397f11e160c95c9674da55ee829cc2a20d08ccc185c7e8a680e66d7719145e`  
		Last Modified: Tue, 14 Jan 2025 20:45:20 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d21c8eed9a243cd32d7dddab013999cb11190e501372649c04afe9d9f080c542`  
		Last Modified: Wed, 08 Jan 2025 18:46:14 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f846d8cbb7e2cb06417f862e8cf924974113d2ced1a09b6d50dfccb1cacd9f21`  
		Last Modified: Tue, 14 Jan 2025 21:04:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1c876795ecb61d15f5efe4bcb11c3f5fdf2896e3298154e998ceb43aca08ebf`  
		Last Modified: Wed, 08 Jan 2025 18:46:15 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dba1885623459a772da592e2561bba1b7472826fc8608c84c9d7ad2642c0fb5a`  
		Last Modified: Wed, 08 Jan 2025 18:46:15 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:7beb010b1566bc8188b3a70f2ed8becc75ef15445425c0fbd75475ceeafa0d64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.3 KB (495321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f2f6cbcfe902abd8f495ef91d1598737d809fedaedeca17f29e2c1ab169a9f8`

```dockerfile
```

-	Layers:
	-	`sha256:41f840dbbc8db47f74caefe4501eddbeeaf016cba9045bf382312c41ebccda36`  
		Last Modified: Wed, 15 Jan 2025 08:43:40 GMT  
		Size: 464.4 KB (464426 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5655f329193cd9ee8e2bdcd9a89cd812764f9b127c8328ef4b31c43af4572714`  
		Last Modified: Wed, 15 Jan 2025 08:43:40 GMT  
		Size: 30.9 KB (30895 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.20-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:a50aa1511d1a1a763c27fb0d0e143847baeab3bdd2b04595facfbad3aab4d920
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5905536 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e5e3a275a347d4f6f21f7a0b48afed0d9657db26002e49298ab985e41bef787`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
ADD alpine-minirootfs-3.20.5-aarch64.tar.gz / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
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
	-	`sha256:0152682790bba2052e0b7dc52872083c01ea53c598fe87e3fe3eab5f9d4228cb`  
		Last Modified: Tue, 14 Jan 2025 20:33:00 GMT  
		Size: 4.1 MB (4090769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34f4f67366d7ed3eeecf4db9f420b1af3fcca7a5738bf972b1e99a6f1de30697`  
		Last Modified: Wed, 08 Jan 2025 18:43:31 GMT  
		Size: 1.8 MB (1810174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb6bc1d08cd9f3ef90a462e966930f90b203297392596a7810bd91f1fc8d736d`  
		Last Modified: Wed, 08 Jan 2025 18:43:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b12d344c7bc2a044da5530d98159ef627a396ce731ec02e02b4779c4b37ef58`  
		Last Modified: Wed, 08 Jan 2025 18:43:30 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d89794bca8fd43a9206b2a53125c3edc4c4a2fbd8d4e795421b61ac067aa02d`  
		Last Modified: Tue, 14 Jan 2025 20:33:29 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:685f57786a721fd2c076258ea2df427b5152f13ee322a6e17216b276397eba4a`  
		Last Modified: Tue, 14 Jan 2025 20:33:03 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:876850e427bb633799d790f32738cc2577159ed8acef5a1b35cf81a2a3b6cf70`  
		Last Modified: Wed, 08 Jan 2025 18:43:31 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:36e30f7422460b1c6ce81bcc753ce3a9b45235cbbf2cd8767d6a884d8ce9d67d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.4 KB (495418 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77dc430fe77b21052c80d3f22398cbff47ad2f8591b0043dd24aa8db60e70897`

```dockerfile
```

-	Layers:
	-	`sha256:1783d1a41954320faab7b1314d54d23be9103364fb826d0c3b5c8bd28a8a6e00`  
		Last Modified: Wed, 08 Jan 2025 18:43:30 GMT  
		Size: 464.5 KB (464470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dd0d5daf175851378f3f2f1251962a64db8d5ea0bc1bfea0f8264465e3e17f0`  
		Last Modified: Wed, 08 Jan 2025 18:43:30 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.20-slim` - linux; 386

```console
$ docker pull nginx@sha256:b34f645f3044a57c51581637d3f06beb477059d1a028db89ae1657155a3fd4ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5460372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec37b23d3d88feeaeddbdbd90372617f4d33e243ecd9ae323f60b38d7f764484`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
ADD alpine-minirootfs-3.20.5-x86.tar.gz / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
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
	-	`sha256:6d632fc6244662e41ee3b3f29090684a520e615dc5c282638a7587366dcd4fb9`  
		Last Modified: Wed, 08 Jan 2025 17:23:34 GMT  
		Size: 3.5 MB (3470969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f5f71716912081f6b04ac4cbbc409f86da5eeb23327beb5e0e184f2dfd45231`  
		Last Modified: Wed, 08 Jan 2025 18:00:47 GMT  
		Size: 2.0 MB (1984800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf1c03a8b33398850861f7c647c1a048983b6ed76b7430d7d62f7845f81c53b1`  
		Last Modified: Wed, 08 Jan 2025 18:00:47 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:609c0239d7347943659d765b92299bcd40187ed20c05a2cbbabbbb635af684cf`  
		Last Modified: Wed, 08 Jan 2025 18:00:47 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c704ee8b5141588d474cfcd30ca053839ef1d35100f746f32680402b4212678`  
		Last Modified: Wed, 08 Jan 2025 18:00:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7151804c84d6f4a49419fd0cea4f4346098122e79209f6118f3e96b56e2edc76`  
		Last Modified: Wed, 15 Jan 2025 02:01:57 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54166ec8942be799540605cff522f336f91e134e9b7b23d81ba6aad39a075636`  
		Last Modified: Wed, 15 Jan 2025 02:01:57 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:15b54bd04a95b455286d372bf0092c7fac864134ac6ca7e52a203c2bef6da8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.0 KB (494997 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:612a9c4538e7ddd3a62092d15786e58cccb896cfbed057d68df8aafb9a178e60`

```dockerfile
```

-	Layers:
	-	`sha256:2ac61c190d2bd0efdd7b7fbf30b7bbc62275b843766b21cb581d41b5ba7f98c4`  
		Last Modified: Wed, 08 Jan 2025 18:00:47 GMT  
		Size: 464.3 KB (464287 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41664456da0b53e831e10595f26a1eea19e8ba70c91e262b4d444cdc25e5afcc`  
		Last Modified: Wed, 08 Jan 2025 18:00:47 GMT  
		Size: 30.7 KB (30710 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.20-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:3583f7c84c51e9e93e4e75c16b20d3e5e36d384476a70763908a1054908fff24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5553984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:759b25e71eda1c6d27f437de2d4ef5bf0692259b8473a2e9dab15aa8aa93648a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
ADD alpine-minirootfs-3.20.5-ppc64le.tar.gz / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
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
	-	`sha256:3383dff810cd4af0350465f92c0a5f925af062ceac665a36e91384093216a7db`  
		Last Modified: Wed, 08 Jan 2025 17:24:56 GMT  
		Size: 3.6 MB (3574406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:230d474824d3a98692c4db1f8fd4fee0df7e931db6548dd2243c7d1eb4660247`  
		Last Modified: Wed, 08 Jan 2025 18:30:17 GMT  
		Size: 2.0 MB (1974977 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ba7e11f71a07c2bdcc6129ee38b5ae4fd03c7f28584d6a966bc789e320334a0`  
		Last Modified: Wed, 15 Jan 2025 02:01:57 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a078ca5635d735a85aca8ee050449cb9dfef02f4db254d7d5c2f2d63066e4784`  
		Last Modified: Wed, 08 Jan 2025 18:30:17 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a65dff001996a099f206b1665957d8207b8c1d0e4fb4306af7d94fd18634529`  
		Last Modified: Wed, 08 Jan 2025 18:30:17 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f98d8fd82d5a8c881e0257afeb0b7b341bc612c3ae70f8b08e1fcd57443ed7`  
		Last Modified: Wed, 08 Jan 2025 18:30:18 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa422795849241370494e05ac5e1682fe7db94bfcb9fe5da1d124614d987a22b`  
		Last Modified: Wed, 08 Jan 2025 18:30:18 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:276c2780a44da1baf067e50e02405b55fd2d98d248f91c268cc80d9727932290
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.3 KB (493313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce2832dd398026c21ccbe95b51720aacbbe2907e2f66102aa70fb644d82521fb`

```dockerfile
```

-	Layers:
	-	`sha256:101638bbebb303aff133f7563463f991c4f3ae72577bab822121427de4f4c90f`  
		Last Modified: Wed, 15 Jan 2025 08:43:42 GMT  
		Size: 462.5 KB (462461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e4b0e7806d7b51219b3011be88f20c3f83f2401fe041588f752ca9377869fe9`  
		Last Modified: Wed, 08 Jan 2025 18:30:17 GMT  
		Size: 30.9 KB (30852 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.20-slim` - linux; riscv64

```console
$ docker pull nginx@sha256:0c3a61054dd6ab832f70206839bfc601992c92e851e156188b126cff425efb4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5330709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20c04addae8646089cdd98b919b9f7ed9e85e3dc79e638ebe2dce02b85f28d7c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
ADD alpine-minirootfs-3.20.5-riscv64.tar.gz / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
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
	-	`sha256:34b7590cc8ea3b21e8c3a0d69270b822d3ba63bc58c6cf0e36c987c95b18eb8d`  
		Last Modified: Wed, 08 Jan 2025 17:49:41 GMT  
		Size: 3.4 MB (3371926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:237bd1b926f61c549b4ebf1eb45078904fbc6ba68e056d910b94a1bcdc3998f3`  
		Last Modified: Wed, 15 Jan 2025 02:01:57 GMT  
		Size: 2.0 MB (1954175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e5b9a0b807ef783d90c052d2a938e26eb441b36a3b377cedf4d6da85dde7077`  
		Last Modified: Wed, 08 Jan 2025 22:00:26 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06f8ba1c997b2680c311d88180dd2072896079931040ad9a824cc1874ba3b329`  
		Last Modified: Wed, 08 Jan 2025 22:00:26 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a77ae209607dfb76887ed972444fe52e0eea63862111a78081e16be44339fdb`  
		Last Modified: Wed, 08 Jan 2025 22:00:26 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9eb1d508ef12219e21f1e47df11c92f78770f38612dedefd82027213de96836`  
		Last Modified: Wed, 15 Jan 2025 03:05:03 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:918ee1b5c736470e6a5d99dff0e22ad9712167f015731d067a2207b05587b959`  
		Last Modified: Wed, 15 Jan 2025 02:01:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:4fce42abd3e3fd2a0d13f29441e0585897db6bab8c977ce4cc10faa2ece678f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.3 KB (493309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39292e9f17780ed3fc2201387906ec3987dd795e92867140de9555077b1d72ed`

```dockerfile
```

-	Layers:
	-	`sha256:4e118a88aab219e79c4df298e04989c69b8bba9e4e38277d2d65312c4876befc`  
		Last Modified: Wed, 08 Jan 2025 22:00:26 GMT  
		Size: 462.5 KB (462457 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1c48390aed303fc039d2453fcffc0b35488a989e838a6fd72178a41d2c4eb1d`  
		Last Modified: Wed, 08 Jan 2025 22:00:26 GMT  
		Size: 30.9 KB (30852 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine3.20-slim` - linux; s390x

```console
$ docker pull nginx@sha256:de6e9969674ec298cf265494ac7ba9dbecb33f978c9670b4b03a46660639816a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5472472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce6501b5c6e8f96620eebe77003c08751b513df844e31c5d6b43d72ba851bfa1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 26 Nov 2024 18:42:08 GMT
ADD alpine-minirootfs-3.20.5-s390x.tar.gz / # buildkit
# Tue, 26 Nov 2024 18:42:08 GMT
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
	-	`sha256:3e71c43ed556c3ed564b517d9141db651f4134655f96c8731767c14c6dedc4d0`  
		Last Modified: Tue, 14 Jan 2025 21:25:41 GMT  
		Size: 3.5 MB (3463322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e78ac72de564765e8950608208b41384cffd18a72b4ae558e660909e5de5b521`  
		Last Modified: Wed, 08 Jan 2025 18:32:36 GMT  
		Size: 2.0 MB (2004552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd22f93c01a0a25eb3417a5149cb34b92ea4846601e62478545b3cce8e368f30`  
		Last Modified: Tue, 14 Jan 2025 21:22:09 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a6425795ac5d2b1209a7034031cd7fd973003a2a9849269215fe4c118195ae`  
		Last Modified: Wed, 08 Jan 2025 18:32:36 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1af3a173d83436aecb70ed5c924dd982cc1b6cb4930d4cdf19ed6fc16fd9846`  
		Last Modified: Wed, 08 Jan 2025 18:32:37 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9436b1b6f1bbf6e0326c0e8c71ed5d846fdd6f014481918c871a41a4295e70b9`  
		Last Modified: Wed, 08 Jan 2025 18:32:37 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:473885e3fb234f83efac17af4d90aa88295f98d9ca81ca04113477504bf63663`  
		Last Modified: Wed, 15 Jan 2025 01:48:46 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine3.20-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:131376fde603ac0d1be25b2cf3bd4fcbc24b670eaf622bdaaed0d1edad9b80d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.2 KB (493162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0c0b34ab07bf6c21268d61a9cc6c4e38b462542667071f0f89bd90e0cf2cef5`

```dockerfile
```

-	Layers:
	-	`sha256:91c072877ae818449b6e4d29014680bc49d7c313e555d83febd25c4c469c36fd`  
		Last Modified: Wed, 08 Jan 2025 18:32:36 GMT  
		Size: 462.4 KB (462391 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:798455a27409c037e72cebfb20378c099d75439d7817006fdd0f45b4a66bd531`  
		Last Modified: Wed, 08 Jan 2025 18:32:36 GMT  
		Size: 30.8 KB (30771 bytes)  
		MIME: application/vnd.in-toto+json
