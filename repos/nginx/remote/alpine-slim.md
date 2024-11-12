## `nginx:alpine-slim`

```console
$ docker pull nginx@sha256:9ebd266ba0ddab1bf6c0f7580bb53f373bf5ac137ec02430169d20c4c139c70b
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
$ docker pull nginx@sha256:bbd86dd5c396c076dfb899e207ae75a095c7bd7ff906bca5247e07536b610034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7668688 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:452bf8598f8723bcab09ab49b2d2994145dc328a56097b7ad7ac1cbcaf63f932`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86_64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:da9db072f522755cbeb85be2b3f84059b70571b229512f1571d9217b77e1087f`  
		Last Modified: Fri, 06 Sep 2024 14:39:08 GMT  
		Size: 3.6 MB (3623904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:795a89dcc4f004d517a7834a19e066200cda1a9d8258bfbca3d9410259261053`  
		Last Modified: Tue, 12 Nov 2024 02:03:03 GMT  
		Size: 4.0 MB (4040188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ad567d3b8a2ca8d6e3cbd00b3b78feafbb1c7e7e2ce1492648ea01cdd06d50d`  
		Last Modified: Tue, 12 Nov 2024 02:03:03 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e8836903ab0b0428bee291efed146b37ed4aee8b378e7a2b2fb8ad407c9947`  
		Last Modified: Tue, 12 Nov 2024 02:03:03 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:276e8818f0df64d1efab55dcac66a8ab3073b584adc8e1aeef8b3479f935eb04`  
		Last Modified: Tue, 12 Nov 2024 02:03:03 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20212ccf8a7aa043bba568bf8ade4778a0895439cbe76033682d6a05a7ebdd92`  
		Last Modified: Tue, 12 Nov 2024 02:03:04 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3917e8bc7be0dd282c01911e9c34a9931f7ddcd78d3acfb5b45e3378303840f1`  
		Last Modified: Tue, 12 Nov 2024 02:03:04 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9682751ec926c9a2c8ca6f3021f0d3b96e56e03a94f87a1cb26b126a9285836f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.9 KB (495920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bde20d5228d82d740093127741c016d83938d711a158530994c8dde68e49c6`

```dockerfile
```

-	Layers:
	-	`sha256:5b5091e65ae55fd438821a7574446f3f918b7f34c1478fc76e52de6348ef07bf`  
		Last Modified: Tue, 12 Nov 2024 02:03:03 GMT  
		Size: 465.1 KB (465148 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ef4b5eb216e3491d54eb3a8dd55ff0cca33ac235ff06b29ab442d0718cf95368`  
		Last Modified: Tue, 12 Nov 2024 02:03:03 GMT  
		Size: 30.8 KB (30772 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:2903c27e3aa9d046f5f683e54fd1d1250f8b66adacad5e44faa23cd3773bfe8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7214897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2c3277ed6375d35acf03e06286314c05c40a71dcbcdbec278a024051aa9dbc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09c550e65d3988baef17d7cc49f768e980523223dee7270c402eb6db45dc4e8d`  
		Last Modified: Tue, 12 Nov 2024 02:45:11 GMT  
		Size: 3.8 MB (3843703 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9e469b7a136bf1f262ac620e43d015dc74f079739224b9a64c4d249fa4d83c6`  
		Last Modified: Tue, 12 Nov 2024 02:45:10 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b2db11dc0ae5c6183ba6385fdf31c622380f60ad3e04c1b8adab77608e2316f`  
		Last Modified: Tue, 12 Nov 2024 02:45:10 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6633d9e0de79a7649e041668adf03aad74141143dabb9ece94674532dc59c64`  
		Last Modified: Tue, 12 Nov 2024 02:45:10 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f1369514919c881b022e1bf8077ba3f13c7307e5846cb9a57b728f337d6f53a`  
		Last Modified: Tue, 12 Nov 2024 02:45:11 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:471918f939c26c58225aab7497e49d884ffdc2199c140d54ec4eca5fe3aa2a42`  
		Last Modified: Tue, 12 Nov 2024 02:45:11 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:588e98ad4f060a5138d187fb1cf7fb851058273054daaede5dcb5710810771ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.7 KB (30681 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1af83fa58a61d3ddee10db01281d136071e30cb7497a0934518a2b070eda401`

```dockerfile
```

-	Layers:
	-	`sha256:fa7258806835e0723cccb8186ef2bcc550b9908b01e1d10b36390a8b252bbf1b`  
		Last Modified: Tue, 12 Nov 2024 02:45:10 GMT  
		Size: 30.7 KB (30681 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:a5e37ed4b77c98df3276c147c920e7bbde9c83a3a115b03c5b502498f1da345e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce05f7a82da09187630b71b07ad2a805465bcec4344574f17ecb4e35a0f5c097`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57fdb1b875c903cd62e482306a0d9c5fa4a0d7115ddf0d4a53db244b64e52d22`  
		Last Modified: Tue, 12 Nov 2024 02:56:49 GMT  
		Size: 3.5 MB (3528090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d14e2d99a31ccc63b1fbf88b72b87c7db8d327af21e127b41e545c9955b1425`  
		Last Modified: Tue, 12 Nov 2024 02:56:48 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dc86e92e35641fd11f682792d975b9c2fa673d81abc398749364b371f17fb4a`  
		Last Modified: Tue, 12 Nov 2024 02:56:48 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47bf772197642b6c37976055f117d42faa28a5a22dfb98017bc2aaa38a13653c`  
		Last Modified: Tue, 12 Nov 2024 02:56:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6bdeada5e30b23b6aaf2022fac832cdd391c2ec7745311fdf7245f87f4d8239`  
		Last Modified: Tue, 12 Nov 2024 02:56:49 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c253f97f119756f81524c98c637d48d2a61840babcc34d4e91b43ac2dcc9a6c4`  
		Last Modified: Tue, 12 Nov 2024 02:56:49 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:e62c57f85ad80decf208360b2df90fbc6d0dd4a34c37b3445199ee4c7fcdd2fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.1 KB (496128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1a605af19a1b4866e39d5fc7f11999d0c61a21a278899a0f8824c25bbe9f422`

```dockerfile
```

-	Layers:
	-	`sha256:724d82ab9560f0113fafb1d4d42821f51f3deedfcf7a7f5c7050a8a4196079d3`  
		Last Modified: Tue, 12 Nov 2024 02:56:49 GMT  
		Size: 465.2 KB (465232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4dde24b24ca75faec3660c2c3c30f5029ee1b73758c7374339c0ca92bd28640`  
		Last Modified: Tue, 12 Nov 2024 02:56:48 GMT  
		Size: 30.9 KB (30896 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:22289236608e607d47039f316147b4e21005946ce6ab342305511cf99303ef56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.6 MB (8577698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c464d66ccc9fb3c3a3c446c3cdf0d8ba59d0388a614a9d779bc77c777a2dbef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d2c03a3167914043dfbd615fba736c71324327141f51ba844d17de54976bb37`  
		Last Modified: Tue, 12 Nov 2024 03:27:16 GMT  
		Size: 4.5 MB (4485380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdbd9ce708a090def7f2e9d7cda073eef8f645e92d9e1139b55eecf36ad99431`  
		Last Modified: Tue, 12 Nov 2024 03:27:16 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9db6e0a97dc7029b175afe958f5ac34d13e820501d3ce3b5b99b2e7a922f7019`  
		Last Modified: Tue, 12 Nov 2024 03:27:16 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:907a2bd54803da52254db1fa636dc39fd6cfd936515058322ba6993c96d520c4`  
		Last Modified: Tue, 12 Nov 2024 03:27:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afcc754f1e6208f8da0acd8417cf8fa9b8f152f567870ec622b32271156f53a2`  
		Last Modified: Tue, 12 Nov 2024 03:27:17 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad729297a2b4eebbc1b8d1a15166b7f6542002ea83397c908c9224fc381db6c`  
		Last Modified: Tue, 12 Nov 2024 03:27:17 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:8b9da5e05d30bcc04db1c25b2ec578c5e94b933891309bfe44b8ebd8242179e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.2 KB (496224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12d17f5dea2e053a20fa7c066cb03fe8e175d7565d817f80d9a1b57adff611a`

```dockerfile
```

-	Layers:
	-	`sha256:4a7daa96c3f3f94cc6496c1e39954ff94a773bb638b484a2e6d3c9d7428a5463`  
		Last Modified: Tue, 12 Nov 2024 03:27:16 GMT  
		Size: 465.3 KB (465276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db7b3db5d6e9507acb9ac9569e8aa7e8763e4600c5ee357224fef75e33afda72`  
		Last Modified: Tue, 12 Nov 2024 03:27:16 GMT  
		Size: 30.9 KB (30948 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:0bcf1e55ab42f51ce884db3d7cb7f7ba72f2624a837ad94ed9f7e1f89d6678a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7555077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b3450e6241b7896a13fff1d209e6009e1550b6e56038bc453c0e0ba0b0e13b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-x86.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9d36213c2c70043b8757c7d7ef3b21782d1ad5b2dd6d50df305e14054d6a1cb7`  
		Last Modified: Mon, 09 Sep 2024 07:03:56 GMT  
		Size: 3.5 MB (3469219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07dec20a1f12e94a4d5af95e377de7d77f3244579cfb3ca8e83d25e11d78d9e0`  
		Last Modified: Tue, 12 Nov 2024 02:04:39 GMT  
		Size: 4.1 MB (4081259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a949b43e642c715fce2e6addc4bf096facbed53d471ac6c0d85d8e128a25cf52`  
		Last Modified: Tue, 12 Nov 2024 02:03:26 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad7de96ab26ba62a5c339287217d406fe7971112a3b2468d6a231f23bdf34fc`  
		Last Modified: Tue, 12 Nov 2024 02:04:38 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:835b1867ce5fc5e22a641c8a8efab8c743e565075273c79bc22d4afdd8850365`  
		Last Modified: Tue, 12 Nov 2024 02:04:38 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab1fc9daa7c384a460584dfffe814513d09c32f7dc27ac74737a7775e1f4cd`  
		Last Modified: Tue, 12 Nov 2024 02:04:39 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db3943829aedbc39c63be841e74a327cc8837aa37f81639645939c21d276c268`  
		Last Modified: Tue, 12 Nov 2024 02:04:39 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9d1da57a5fcc403678006a8e75f8e0ffe6f87f7199d7014767df3e111b04664d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 KB (495802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2a191021ce19c34fa859548713d6df36d765ab4b268e4ad4b5e822ed5e625e0`

```dockerfile
```

-	Layers:
	-	`sha256:91a5402ee5cc413276947da2b2d3ecd74e062ff3b7dfecdccde1384701c4ee15`  
		Last Modified: Tue, 12 Nov 2024 02:04:39 GMT  
		Size: 465.1 KB (465093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07b57306390f421ebec28d2e8f0d5fd8422ff8acabd8df8cd1254a21f35a9bf6`  
		Last Modified: Tue, 12 Nov 2024 02:04:39 GMT  
		Size: 30.7 KB (30709 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:3dbd320a8fbcecacb4073bea4f13c6c62ba3f08835d939b7b67ab3255fa9f74a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7679439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6c5440da79e7c6d463a992a76b9b1c1eeffb9e26b6bbced9c7a09a94fe66749`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-ppc64le.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:22892cdc5e9ff297ac012c2fbe3c12724a3cf4d0a55f5f03f95a7f3ab3e77e36`  
		Last Modified: Tue, 12 Nov 2024 00:55:07 GMT  
		Size: 3.6 MB (3572459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b21f5136bd97029ba61210efc7eb6442602c40db129a80da7e0fdbdfa673c48`  
		Last Modified: Tue, 12 Nov 2024 03:11:19 GMT  
		Size: 4.1 MB (4102382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb937c7ab8af42868263a87fa11cfe55ce10eb17cbda8a27ccb251137f680804`  
		Last Modified: Tue, 12 Nov 2024 03:11:18 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a311c4d2d7175758fa5d475b3c015c6179d570278409a539fb6b1b39c604a286`  
		Last Modified: Tue, 12 Nov 2024 03:11:18 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2d24b8ab89a919d7277ab1e01b5384fa0fc5111bbdbc97c89d45429579b530`  
		Last Modified: Tue, 12 Nov 2024 03:11:18 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af6c37a681f0ba5f280ef2f674a35c376985f9ed6ae981d41da1959c3fc95b64`  
		Last Modified: Tue, 12 Nov 2024 03:11:19 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3633d4c27caae3f535a76ce88722cf102dc8f42c69dcdd3edb49c73025f853b`  
		Last Modified: Tue, 12 Nov 2024 03:11:19 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:37d85aad5fdfc37c42123ee97d99b4745c7dbef06c4819c7e71bb51552fac168
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.1 KB (494116 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12f85a8f5bd73b19f9f7061060cfea14abad410cb0d5b550d8e052dc1bc24601`

```dockerfile
```

-	Layers:
	-	`sha256:cff8e9e8a9cf6f81abc84b094f036fe5480f9634f701e49188a587eacb38ad1d`  
		Last Modified: Tue, 12 Nov 2024 03:11:19 GMT  
		Size: 463.3 KB (463264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc20561bc8e6c66f383809e7ded28643acca17d04608e4db2e1a2eb807c1c94a`  
		Last Modified: Tue, 12 Nov 2024 03:11:18 GMT  
		Size: 30.9 KB (30852 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:36d3168c8009ae0f2fc1fd2183395cc2eef3368cd228b52faab9766bc3824a7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c03a4040549089229a0e3645fd3e740b6b9f3c6aee6e33bddcffb89f79ac0866`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:294fbbd88f8cb23069c5ca1b55e459dfcfadac238e13ebbb92c7d2ce8a43cb45`  
		Last Modified: Tue, 12 Nov 2024 03:03:28 GMT  
		Size: 4.0 MB (4024328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93c69941d21d3e1a4c2e5334fe9466906d6d4128535c0c381e425af233683c9`  
		Last Modified: Tue, 12 Nov 2024 03:03:28 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a33ff2f5b804a90e566e3167afa78829a097c615987ef63e91488ed2c9b7fde`  
		Last Modified: Tue, 12 Nov 2024 03:03:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:330c079f3f96298a6c5173035406c394055706b92cd2b9d485216fe9313aeef3`  
		Last Modified: Tue, 12 Nov 2024 03:03:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6189f48fd8c80305d3e127719c3a3b21901c41bfa5deb0808cb5c93b0885c89b`  
		Last Modified: Tue, 12 Nov 2024 03:03:28 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:153dd15449c1d6cacdc0fc769e31ac336d616844ef856dd4a57ad4dbcd0943bd`  
		Last Modified: Tue, 12 Nov 2024 03:03:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6ea37b6664f3d5d4a0984e6ce511994a2c47a9711d247eac4c794dae03e54031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **494.0 KB (493966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f571b2da32cf175a8bbf00d00ed1c8e738f51ff3a6ab5756dad69289e9794e28`

```dockerfile
```

-	Layers:
	-	`sha256:95ec2209d24e3c90e6b584a0b0f93054cbc0ba66475ece247034ff8039748926`  
		Last Modified: Tue, 12 Nov 2024 03:03:28 GMT  
		Size: 463.2 KB (463194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25f18e464bf008599f77f96b16abde289e75a6ae33619ddda722e93b86df70bb`  
		Last Modified: Tue, 12 Nov 2024 03:03:27 GMT  
		Size: 30.8 KB (30772 bytes)  
		MIME: application/vnd.in-toto+json
