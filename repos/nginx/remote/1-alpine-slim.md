## `nginx:1-alpine-slim`

```console
$ docker pull nginx@sha256:7170d29ee1275b1f12b4cb1dd2a98e5b9473766151dba6615844f19684080b8e
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

### `nginx:1-alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:3bef9528bb5cea997fb7e0f106d2a4a6142cd0e8e8068f4cb54edc148b872fe7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5309304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fd4619865c41fc92e863b78db34771d0af19df865c6eb930efd7d4ad07d7e11`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NGINX_VERSION=1.25.4
# Wed, 14 Feb 2024 18:24:57 GMT
ENV PKG_RELEASE=1
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"79bf214256bf55700c776a87abfc3cf542323a267d879e89110aa44b551d12f6df7d56676a68f255ebbb54275185980d1fa37075f000d98e0ecac28db9e89fe3 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Feb 2024 18:24:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed3e62e73b33c9cfa4b253060771e4a9eebb751ab438052f197e847b4553a9ac`  
		Last Modified: Fri, 15 Mar 2024 23:55:18 GMT  
		Size: 1.9 MB (1902176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5126dce06df729f9a22956013e160f8b581d47095beec332d647a5c1119b2411`  
		Last Modified: Fri, 15 Mar 2024 23:55:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d0dd2dc2265a581798226f7c79d134ac797f42db3f934dd4af1d38a6b89ce5c`  
		Last Modified: Fri, 15 Mar 2024 23:55:18 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1ab92f023179da00446365a60daa60d72a1edeb697fb81811e086eba2e0170`  
		Last Modified: Fri, 15 Mar 2024 23:55:18 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6eba808ac059320c42179a6590b021f8695d3f12c2afa8745e219f635acf19d4`  
		Last Modified: Fri, 15 Mar 2024 23:55:19 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57038e85fbb88e96e34a84b125e568f540437561adb363fa791ff9e94e153dc1`  
		Last Modified: Fri, 15 Mar 2024 23:55:19 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:08a2d68e663c8584caf1876b2695e53209006a6b29de2e0e525fc7c17e62a3ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.6 KB (869578 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f0ecf5bd8db878d65cbeba634f6a047bb4b01d6914a8588a096dc75836bcde0`

```dockerfile
```

-	Layers:
	-	`sha256:bdaceffe11ccb468b3eb928e61dbe5588880355e8e59a4e4668b212e51013c73`  
		Last Modified: Fri, 15 Mar 2024 23:55:18 GMT  
		Size: 838.8 KB (838808 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06f452dd94d4551acee8db4eef7b8f07be8477b4ba19108db563553ae3636584`  
		Last Modified: Fri, 15 Mar 2024 23:55:18 GMT  
		Size: 30.8 KB (30770 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:8936311ee08b4cbcc542215ac2baea20c448dd6a256f97a56124dc30a2aaf6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5183659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31f8a20db45e9f663c891cba4c01c5d350bc24bddbacfe8d5324b03a5ce26341`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NGINX_VERSION=1.25.4
# Wed, 14 Feb 2024 18:24:57 GMT
ENV PKG_RELEASE=1
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"79bf214256bf55700c776a87abfc3cf542323a267d879e89110aa44b551d12f6df7d56676a68f255ebbb54275185980d1fa37075f000d98e0ecac28db9e89fe3 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Feb 2024 18:24:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a56abc35c5cbc4e96f63d308964a4e19f607c979ab30436f088f5a234e6d8551`  
		Last Modified: Thu, 15 Feb 2024 01:24:47 GMT  
		Size: 2.0 MB (2032010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d586e872214b15950f86cab8b960b52dea0a6e0247b5fa89193acf982785cf9`  
		Last Modified: Thu, 15 Feb 2024 01:24:46 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9413f5930334deaea00bfedc771f8c32b2c7326da59f815922b04ea05a380de7`  
		Last Modified: Thu, 15 Feb 2024 01:24:46 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197a406898e34d2dab8f197f7a71c2f69a0d9465a3c0cdf91e2b639e675405a7`  
		Last Modified: Thu, 15 Feb 2024 01:24:46 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d611649b9b677f30ede1aaad546cbbb8a88a4db13ed60539de4e8033f2f74ff`  
		Last Modified: Thu, 15 Feb 2024 01:24:47 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550939a9bfb84257e1bd5be4001216c336f05bba24be3821ff01609b0e1f3723`  
		Last Modified: Thu, 15 Feb 2024 01:24:47 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:067c84e1fd618923f89d085e7e22b8907051e9885f4b208cbe56bab267bac812
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.5 KB (30507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b7d502cb9a69c56c3dcc1b632fa1e19c778c834cfd86a66c2b6c0b3e1d2253`

```dockerfile
```

-	Layers:
	-	`sha256:43b48707b219e526e4db809a455497bffe56d0d9198ddf87752d1f2d3622f456`  
		Last Modified: Thu, 15 Feb 2024 01:24:46 GMT  
		Size: 30.5 KB (30507 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:34f2786a77120c166f83c737d26d433228e1ffa0400c06cd9bb0706077797a3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4775968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00915f42bfd5cfc85e8c7db0260f1c21eb983d37ccf26424e158db089c6091b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NGINX_VERSION=1.25.4
# Wed, 14 Feb 2024 18:24:57 GMT
ENV PKG_RELEASE=1
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"79bf214256bf55700c776a87abfc3cf542323a267d879e89110aa44b551d12f6df7d56676a68f255ebbb54275185980d1fa37075f000d98e0ecac28db9e89fe3 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Feb 2024 18:24:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101771643a485165c2cad2c3d066c032de539819352463a937f7aacba7dc9485`  
		Last Modified: Thu, 15 Feb 2024 22:04:32 GMT  
		Size: 1.9 MB (1869988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba1344b1bebe539dca0e68a0bee50368d093529c450eeb3fba3b1fbc7f31c3e7`  
		Last Modified: Thu, 15 Feb 2024 22:04:31 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e69cd06fec2e5b634eb93bfdf554dacc2a370e2dd04f9d1fb06ca143787f1ede`  
		Last Modified: Thu, 15 Feb 2024 22:04:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63cc04c8dc44f51f81d7b719e2474a2711614accce15a6296d37174e6caa2fd8`  
		Last Modified: Thu, 15 Feb 2024 22:04:32 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f56b858a9febc42286d37b00c75df63349225b6679427e4fe28fb48327cdbd`  
		Last Modified: Thu, 15 Feb 2024 22:04:33 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60bce3e2b8369dbff9a087414156146becb5cb0ec8447990719e10129d8c8d63`  
		Last Modified: Thu, 15 Feb 2024 22:04:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:1c02d5ab067d79f87e883b2a02f54c75ed34e6cd8c78aa628641c952c820a2b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.2 KB (732238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586b53df7fcbf1387c0ea28343d1a2244c549531c0fac448e5c75b2f9db67451`

```dockerfile
```

-	Layers:
	-	`sha256:019675aadb89f982c8f3973988c1e2f7e8c075ae23fcfc48b92ea7e8aa6ced18`  
		Last Modified: Thu, 15 Feb 2024 22:04:32 GMT  
		Size: 701.5 KB (701516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:98a0623d291de9f2fc49dc2499ec262a5dff3d6dc722ddb11b17f02f12d7735a`  
		Last Modified: Thu, 15 Feb 2024 22:04:31 GMT  
		Size: 30.7 KB (30722 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:3e669b4d467ba97943244adf552a85edb03d2a06415f9e3492645baeed051b6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11ae9a426ecc7bc7a554af0037dc7f23352fe454c71387ec1abdc9f0ca0aa5e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NGINX_VERSION=1.25.4
# Wed, 14 Feb 2024 18:24:57 GMT
ENV PKG_RELEASE=1
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"79bf214256bf55700c776a87abfc3cf542323a267d879e89110aa44b551d12f6df7d56676a68f255ebbb54275185980d1fa37075f000d98e0ecac28db9e89fe3 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Feb 2024 18:24:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41ec95e7228015faee4039fac3545f92994644f7bfd3fb66ca4e8366dfa8c80f`  
		Last Modified: Wed, 14 Feb 2024 22:55:01 GMT  
		Size: 1.9 MB (1926774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da07ba3995b1739c1d95dda0f08dca43c47b45e8b4e9343be19f62444f62f54c`  
		Last Modified: Wed, 14 Feb 2024 22:55:00 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7876903e5e91b56b24250a8b2c2b99d439fd600e1a6d3edd77913995e538152e`  
		Last Modified: Wed, 14 Feb 2024 22:55:00 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11dbdcc188e01d9bb7524ded069f8dd9c0908dc385f8dc3a89585f7e99ecb2eb`  
		Last Modified: Wed, 14 Feb 2024 22:55:00 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e535f861b52be4086f769e9a4a1037e18ee1d77cff03b22b15c770b49a90b6`  
		Last Modified: Wed, 14 Feb 2024 22:55:01 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aeefeb1662b2d2db93a20132608f763eb9c71b43efa577a1c532ae4336ce5fc9`  
		Last Modified: Wed, 14 Feb 2024 22:55:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8bf47c637fa659624159771c61969e0adaaeca0687c40260182be50281d93aaf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **732.1 KB (732081 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b154b49677b648d87895c2da5ae93a02b0a184bd64be5b5b2f2eff42f7f4a8b5`

```dockerfile
```

-	Layers:
	-	`sha256:a31fde610421815901f3997f1bd3d4e04635921386308ee6a484f2d8da0aa1d6`  
		Last Modified: Wed, 14 Feb 2024 22:55:00 GMT  
		Size: 701.5 KB (701455 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59f53bbaba57b06a6124279e3b2e8c29fe6ebcf4a948c35da9b1ceec941ed550`  
		Last Modified: Wed, 14 Feb 2024 22:55:00 GMT  
		Size: 30.6 KB (30626 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:2983b2df0205c83d540e7eda9b1323d31aa65229aed10828782e0275de44168c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5343962 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbdc7d9dbcd7b677d9f3f581f46a2e033dc4eee37f1ab8c41eb9846d010a0806`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NGINX_VERSION=1.25.4
# Wed, 14 Feb 2024 18:24:57 GMT
ENV PKG_RELEASE=1
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"79bf214256bf55700c776a87abfc3cf542323a267d879e89110aa44b551d12f6df7d56676a68f255ebbb54275185980d1fa37075f000d98e0ecac28db9e89fe3 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Feb 2024 18:24:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:617710e6642bdfcfb78366cdc23fc3d8bdf1d891b8cf731467b7f88878d038f9`  
		Last Modified: Fri, 15 Mar 2024 23:56:51 GMT  
		Size: 2.1 MB (2100302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc49e3807b6617bd496ad2624f4ee7232dea8981f2f141e04e20dd305d3bd14c`  
		Last Modified: Fri, 15 Mar 2024 23:56:51 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:881e1a48bd974351c1fee51ccdfd2357f4b058930ea7b4a7e2210ac7c710e76f`  
		Last Modified: Fri, 15 Mar 2024 23:56:51 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc8f36046cc2975bb13834ee76ea2105db2c4f73c0302fefc83b2dd5298dbd3`  
		Last Modified: Fri, 15 Mar 2024 23:56:51 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7c3040540b51e9040d2490351a02a95a4fbd035d68f9130bc4f0fe05c4bf1a0`  
		Last Modified: Fri, 15 Mar 2024 23:56:52 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa9255deb1c46af0539657a209630ed0add92960b7d6d80a124d9ec56c87f8fb`  
		Last Modified: Fri, 15 Mar 2024 23:56:52 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:7e2430e47f95935ec67a1e87ad6f43a40fa19f28e9ede29dd534da3b574fbb76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.5 KB (869464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b358a164eb35f87f0fde8ea60bb3b6d5116b7dde0aeb992f5dde7aed197d190`

```dockerfile
```

-	Layers:
	-	`sha256:44a6aa1bb3c25f805b9399b37a3ce7d10377b17e7c221eb6da4e92cc2fbcae42`  
		Last Modified: Fri, 15 Mar 2024 23:56:51 GMT  
		Size: 838.8 KB (838753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43228ab0546c77ffd44a691d82d11f2cf3d979db3d8f883e383a3b111246b37c`  
		Last Modified: Fri, 15 Mar 2024 23:56:51 GMT  
		Size: 30.7 KB (30711 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:ab7c7c4ac0d7e43868c57d9272b82a628dca92e709b992b8753bdd09ffe5464e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5459330 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e282d49c61d0971723afa6a940d4d439828cfc0c435814fddac17da6c94642`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NGINX_VERSION=1.25.4
# Wed, 14 Feb 2024 18:24:57 GMT
ENV PKG_RELEASE=1
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"79bf214256bf55700c776a87abfc3cf542323a267d879e89110aa44b551d12f6df7d56676a68f255ebbb54275185980d1fa37075f000d98e0ecac28db9e89fe3 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Feb 2024 18:24:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0295a50159527a3c14212306b3dce346e126e57f5f574f58ad1e2dfebba3ed65`  
		Last Modified: Wed, 14 Feb 2024 20:19:14 GMT  
		Size: 2.1 MB (2106264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d00b3c83c8f11106b7dbea0a25543b9d6f52ae3546ec2c4030388bc09ea0609`  
		Last Modified: Wed, 14 Feb 2024 20:19:13 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afbabe12658abf750196236a8eab0a4707638e100f26f01aa81b204067aa7270`  
		Last Modified: Wed, 14 Feb 2024 20:19:13 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e036d85c88978810f3ace6b6103122bfa94154b62eeef1b34a61a66eb6685b09`  
		Last Modified: Wed, 14 Feb 2024 20:19:14 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bbc340da4245215a8a4d0074902d4fd7df77edcaef45a9238496507b469ec04`  
		Last Modified: Wed, 14 Feb 2024 20:19:15 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17008479a92b36efb53d8f69db2e034579fc941eecd5210aabc27c1d6807f5f1`  
		Last Modified: Wed, 14 Feb 2024 20:19:14 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9ef46db50252d71028da474e40d528211b8973746dbd32f5f18887ab2ef5e6d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.5 KB (730544 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:776dcd04e6dfeea851f3f43c74c2bb7ac56e0be2b251d06f0c45b04365e4ce40`

```dockerfile
```

-	Layers:
	-	`sha256:598efae8015e9d5b60d15cb0fa82312fed6cb829a0eb7bb61daaf5fd02f6923e`  
		Last Modified: Wed, 14 Feb 2024 20:19:14 GMT  
		Size: 699.9 KB (699866 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88df45fc454a560a1320eba1354a25be7c5a9a0f8e8ef675f79d65acca9267dc`  
		Last Modified: Wed, 14 Feb 2024 20:19:13 GMT  
		Size: 30.7 KB (30678 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:754b911c3dd7b67b171a704f1645a091a58dd9aedec4cba97e4e2345eaa18d73
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5301595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d305c8c797e51d65760c8d8dd43731ec1bebca7e5d8fac432ec3304fabf248`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Feb 2024 18:24:57 GMT
ENV NGINX_VERSION=1.25.4
# Wed, 14 Feb 2024 18:24:57 GMT
ENV PKG_RELEASE=1
# Wed, 14 Feb 2024 18:24:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"79bf214256bf55700c776a87abfc3cf542323a267d879e89110aa44b551d12f6df7d56676a68f255ebbb54275185980d1fa37075f000d98e0ecac28db9e89fe3 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Feb 2024 18:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Feb 2024 18:24:57 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Feb 2024 18:24:57 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Feb 2024 18:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e910419167367efdc216c9ed4ee9deee34f66d1db26bfab76548335e664c96c1`  
		Last Modified: Thu, 15 Feb 2024 22:53:31 GMT  
		Size: 2.1 MB (2079472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320a19e3e04032cec9ef5e91500f636a9b5fbe09e20bdbd2aa90ac9b1b89c3c5`  
		Last Modified: Thu, 15 Feb 2024 22:53:31 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ccfc37a097f3f3be013c216273857eee3d9d4c16707e79d6021538e9bc14829`  
		Last Modified: Thu, 15 Feb 2024 22:53:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03fc0b89adea0a814a9819149dfd6cb856ccf5ed1f5076e1921bbb3ae4d0ddbf`  
		Last Modified: Thu, 15 Feb 2024 22:53:31 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6abbbd5cc56172dd840baacbaef78515c1408d240786bf0936aa1f111cc24b6f`  
		Last Modified: Thu, 15 Feb 2024 22:53:32 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed7d402968ae8fd1dc5647cf75160d425cfb3cdcd88ecc2efd3cce04b4ba62f7`  
		Last Modified: Thu, 15 Feb 2024 22:53:32 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6c7ec396b33d8cadef3be2bbc4392e60caba8a923703675a073a8e0943ef75f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **730.4 KB (730400 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d240a53db2f29e5e8a2e0d14dc8a72d7d7677c0369416dbd00ac0ed10229aed`

```dockerfile
```

-	Layers:
	-	`sha256:433a654b72c40d234348623ef147a4a1f112551d76e512e98fc557958a575565`  
		Last Modified: Thu, 15 Feb 2024 22:53:31 GMT  
		Size: 699.8 KB (699796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f545ace4f720a40b04f6d7e8517e5ca62a396d6e95227224dad4c02c01396365`  
		Last Modified: Thu, 15 Feb 2024 22:53:31 GMT  
		Size: 30.6 KB (30604 bytes)  
		MIME: application/vnd.in-toto+json
