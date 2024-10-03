## `nginx:1-alpine-slim`

```console
$ docker pull nginx@sha256:88a6be6e4f04e3a32cdf6b9fde865b43f5fced6dccbebe066abce73467dc60dd
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
$ docker pull nginx@sha256:16cdd501b42a6501a2aec8c81915540e8b12d4f16f4784918f75bffd293d9767
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5382188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8caa4b9a10d5c81cf7c33ce72cd2556077bbf5930f71c49af0371eaa6dde44d0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:5758b97d8301c84a204a6e516241275d785a7cade40b2fb99f01fe122482e283 in / 
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.27.1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b9fbdf1779186fc02aa59dd87597fe4e906892391614289a4e6eedba398a3e770347b5b07110cca8c11fa3ba85bb711626ae69832e74c69ca8340d040a465907 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:43c4264eed91be63b206e17d93e75256a6097070ce643c5e8f0379998b44f170`  
		Last Modified: Fri, 06 Sep 2024 22:20:39 GMT  
		Size: 3.6 MB (3623807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b19511a843df5d68c62b357426dd4e99e48fbeb9c085260de375065b969561f`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 1.8 MB (1753795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:652d69a25e853e561388e4ea6f55072df1747066277ef8310aff10d601150385`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51676974aef5e1f3c046f2d40fa8e10d03a4c37e962e00f46bcfb5af242e81ad`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb16f69e8876d046e20b50c0873ac84b46e7b60926bbcc72a32765ad981cc732`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb07faa0055e50ddac110c0d0b6286235e9bd9c0d4de00f0dcb5860dd5833a6`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c298c5a0cd21956f1dec93f16c6968b7b009b43f22add9e78d18273bb91661f5`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:457cb98a94865a5c0f4d61865d7d2e14bae8f6f4e650ca24535cf2675c34ce80
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.6 KB (495580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:724587553ca82b71d9afcd6c05d75cbf87d623c22f2647250741b49cfb3b1165`

```dockerfile
```

-	Layers:
	-	`sha256:0b231bb76d886cbaf4d9a7be39511ad74010d5f65ca8e83dadcbdc923396858f`  
		Last Modified: Fri, 06 Sep 2024 23:21:57 GMT  
		Size: 465.0 KB (465042 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77c5decd5d048de474f0781026bef42f69d551c1fb7cef4f9a8729ac0bd1af2c`  
		Last Modified: Fri, 06 Sep 2024 23:21:56 GMT  
		Size: 30.5 KB (30538 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:e2d3397abfcc8267a8a47de6916f93437d8b92d23e0ef667e59a56a6568eee01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5265349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e286c8fbd3261cbcbb8f253460f51ab87b518e1738432fd5324f2ac657456d1b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:faa3509308d5524875c6afec4d4d1a357118aa1587e5485eca63c2907b37d968 in / 
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["/bin/sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 23:51:24 GMT
ENV NGINX_VERSION=1.27.1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV PKG_RELEASE=1
# Wed, 14 Aug 2024 23:51:24 GMT
ENV DYNPKG_RELEASE=2
# Wed, 14 Aug 2024 23:51:24 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"b9fbdf1779186fc02aa59dd87597fe4e906892391614289a4e6eedba398a3e770347b5b07110cca8c11fa3ba85bb711626ae69832e74c69ca8340d040a465907 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 23:51:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 23:51:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 23:51:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 23:51:24 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:97964a4b92f04f720ed681b3ec62b071ced94b08b57765c612866e77a71ec087`  
		Last Modified: Fri, 06 Sep 2024 22:49:47 GMT  
		Size: 3.4 MB (3366506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2e4ed0a9dae89e232b3fbbb0f2f70affa463e27faf7acdcb9b8f6092f0cae52`  
		Last Modified: Sat, 07 Sep 2024 02:41:43 GMT  
		Size: 1.9 MB (1894234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab847db974f518518dce6bcbcd3f42339641ed980fa69f76da90a9f8a3708ce5`  
		Last Modified: Thu, 15 Aug 2024 18:00:02 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d38561f66f075d1888b1c78dc5a3fa02881a997df049efe641e35fe9b8067687`  
		Last Modified: Sat, 07 Sep 2024 02:41:42 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5400f1f39333642ab7362c840765e6645bd95b2d9d807f25f48a0a91c0617bb0`  
		Last Modified: Sat, 07 Sep 2024 02:41:42 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63d87d4bf98fd0264d05318598071a808768b8c276d6b863ce8ecbca4bd48971`  
		Last Modified: Sat, 07 Sep 2024 02:41:43 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd3b7e04fb075f187fcaa4f0a5d97f40f432a6822d5c9c89d2b4817ec720c8a`  
		Last Modified: Sat, 07 Sep 2024 02:41:43 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:da9fcd4b1550a629873607ba1acb896c8543b83e47a36b79274ce04305af60a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.4 KB (30437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ca58160c2584109329b5cd3edebf8e2f0001481717c7d7407c97ce19e67ce47`

```dockerfile
```

-	Layers:
	-	`sha256:4992de32db271447c23dca693c5284df280bffabc087fd94159f89ed4f670eac`  
		Last Modified: Sat, 07 Sep 2024 02:41:42 GMT  
		Size: 30.4 KB (30437 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:a39187d222b413a11df503d08ac012a431fe093d236220ba80d086c3a39cc779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4831250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef3b7d9fe969e07dd1a701c66f85701a295dc2244fa219d789c2d827ffb77254`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 22:08:00 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
# Fri, 06 Sep 2024 22:08:01 GMT
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4748aefb7b0afb1d873f659424542b85987dcb868a80577c902063c91d789b6b`  
		Last Modified: Thu, 03 Oct 2024 01:19:12 GMT  
		Size: 1.7 MB (1731148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a9d9805a2f29a9758bd68c4418e39fafee204d784e4e5a03bd3db09bee2ac4`  
		Last Modified: Thu, 03 Oct 2024 01:19:12 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b4ca40549b767dc49f853e32e8f89d5534127336f9a964b6b9a3deb596c3934`  
		Last Modified: Thu, 03 Oct 2024 01:19:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f11cb3f72331048d9d6e5485fd01b2c63e5783e0dcd687767ed0eaeda5798d`  
		Last Modified: Thu, 03 Oct 2024 01:19:12 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7fe8f3140cd41275f86bde940b377b1da0f81f877572af55bb8fdd46ab5c3b5`  
		Last Modified: Thu, 03 Oct 2024 01:19:13 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07c3a15f77e735b43d0e5d9c1f3b0b519826c94fbff5001d2237655b15c8115c`  
		Last Modified: Thu, 03 Oct 2024 01:19:13 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:ebcbc12d68a9740b0d4bfeca3b1621fa9808410245abfdbc06a89403280621e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 KB (495819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:379451f484ddb949d519d4f9ff1331d4372ffeb49837cb2edfe56c0f0b8c1981`

```dockerfile
```

-	Layers:
	-	`sha256:43f5988ec4f586762a55d1bf62bea81e08fcd53749ff1fe5765ac74c064a77f6`  
		Last Modified: Thu, 03 Oct 2024 01:19:12 GMT  
		Size: 465.1 KB (465139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5305aec596a16effd074d00c92209085c1a7168761e083bdb57689057912d073`  
		Last Modified: Thu, 03 Oct 2024 01:19:12 GMT  
		Size: 30.7 KB (30680 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:0582a0133278f664824892156b9b727adf22ff69eb54899a095ca690d3b5281a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5883937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a7755250ba6e2e26eaab0e691968443f1748742299a7cb4f2ac55fc219a48a3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 22:44:10 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
# Fri, 06 Sep 2024 22:44:11 GMT
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d0e64b3e72216ff3e1ac9a1fb788ea9c67587ee1bce3797ae6c5be0155cd45c`  
		Last Modified: Thu, 03 Oct 2024 01:13:21 GMT  
		Size: 1.8 MB (1791691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:292ed4bc8f565879e35e29edd4cd1d30111b9b3a5a8937d9cc7c49ab19e0f358`  
		Last Modified: Thu, 03 Oct 2024 01:13:21 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:035f342cad58e155d7ade65b4dced1594a85927d2ef492a374adc418ce89d99f`  
		Last Modified: Thu, 03 Oct 2024 01:13:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bc518b1a2c5ad1e95e6070c141cbb905d8edc5af37afad9f5456687dc84e2e5`  
		Last Modified: Thu, 03 Oct 2024 01:13:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db6c7406b65bb9e3444767ac7c577266fd1dec1eb9d6769b15af4da3e9e648f`  
		Last Modified: Thu, 03 Oct 2024 01:13:22 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa00df5b8f8a7912df82033816004271ba0c8a026ead72bdaeec9ccbfa56f0fa`  
		Last Modified: Thu, 03 Oct 2024 01:13:22 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:6905c54001b1c2c3e2c3d99efc916e8f465e85cf5251bfac713d5bfceca5d7cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.9 KB (495915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de7c33c7b7873126480da85fa3b1948d48de3e4fc234514b8bc5caa538c6d71a`

```dockerfile
```

-	Layers:
	-	`sha256:c812767241fee52715fe3ddadecb84e1bb35e22bceff7d74c4254367d2b89874`  
		Last Modified: Thu, 03 Oct 2024 01:13:21 GMT  
		Size: 465.2 KB (465183 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:85c12cf5c6b1d1a69637232b70c57de9599d177195831af9aaf623aed4c3804b`  
		Last Modified: Thu, 03 Oct 2024 01:13:21 GMT  
		Size: 30.7 KB (30732 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:5991dc29b2190aa6aff05f940348202968708fe8a1c8dc82fb3568b5157241b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5439156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38c2885afb5c8bfa319734fb48dcedd263d34bd5f68b330c1d70e374f93f998c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 22:41:21 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
# Fri, 06 Sep 2024 22:41:21 GMT
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c24161e967f1299f3b65f838518cf3378cb2fe47d3557bb1c260ffbaf72cfa7`  
		Last Modified: Thu, 03 Oct 2024 00:59:56 GMT  
		Size: 2.0 MB (1965392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b88b04c9cfb48e20fe0b72aa189810cce0688ad56f50b4f80a85b41d6296b114`  
		Last Modified: Thu, 03 Oct 2024 00:59:55 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92cf4b910b9cdaa15964683eca21384af94f969c022590c91d5c80595697fd73`  
		Last Modified: Thu, 03 Oct 2024 00:59:55 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a20799d40dd576a270ae6213d8c47d367b0133dce94faa63f450a607c7318e`  
		Last Modified: Thu, 03 Oct 2024 00:59:56 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e1547efcd45c61324c79049aa89a61ab805389eda9319c1015b0ad6318d33eb`  
		Last Modified: Thu, 03 Oct 2024 00:59:56 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa6d61abaf7f100ba1f8a6ac85eb1d994dc7c8c37487be50d2db7898b2c81551`  
		Last Modified: Thu, 03 Oct 2024 00:59:56 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:3d1699d1c7f12778c8461b18ba274170be2e73f6c7b9a433a67579aa8e2d9e97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.5 KB (495503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a0c1f4a22b70878e1203849be7e5a00e9386aa34ca3e5970c851137af7dac38`

```dockerfile
```

-	Layers:
	-	`sha256:6c284828ea684226349346951c1b9e9731bb5290b110e2d25390f4dbd80f5b27`  
		Last Modified: Thu, 03 Oct 2024 00:59:55 GMT  
		Size: 465.0 KB (465000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c79f1b4fbc35e816a9e50b192fa4d9f07349770b563de3b4d849c5c669015963`  
		Last Modified: Thu, 03 Oct 2024 00:59:55 GMT  
		Size: 30.5 KB (30503 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:80810109884ab2dd6423d46585ca6343cc794eb437247d7183a427c704138829
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5533142 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04ca1f9f06a954144fadce8e19c4e613dc79e2ff8b095b3b2dfdbdc3023d505a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 22:26:06 GMT
ADD file:c1f14e23acaff59e2dc7a11f65f8fdfbed8be1350a135493a06b692ecefb26cc in / 
# Fri, 06 Sep 2024 22:26:07 GMT
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
	-	`sha256:b5caf700653f785a3409fb40484075ff91a3a7a84b79ad6a91b165589b35fbc0`  
		Last Modified: Fri, 06 Sep 2024 22:26:38 GMT  
		Size: 3.6 MB (3572419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef4d3e1e4361c3b9722ce8c1de86801b6b899a2342b641776515b4f53d528798`  
		Last Modified: Thu, 03 Oct 2024 01:27:03 GMT  
		Size: 2.0 MB (1956122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b2e44325368b5e2367cee1b5ea5eef5c7c680a66762fef1fce8372ac0a2d8ff`  
		Last Modified: Thu, 03 Oct 2024 01:27:02 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b7a49c2d3d2ee793effbfe747b6e9b65f97f3cf71742c51def7d8d88ddb990`  
		Last Modified: Thu, 03 Oct 2024 01:27:02 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0f76f773dff2e760b88da1bc81dbd20780eecae29f294bf10b1c658ad880d43`  
		Last Modified: Thu, 03 Oct 2024 01:27:02 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdec65782c44cd4ee562d38191719a7332200afde201cc68a6ee7229c2021390`  
		Last Modified: Thu, 03 Oct 2024 01:27:03 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd71e1d7011a82545035e42b2f8e8a19284a147da41136d5e61ee649ef1e56e3`  
		Last Modified: Thu, 03 Oct 2024 01:27:03 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:057a82157314334169a670f11b8d38a8a05a558d477af83b89ab494adf96e684
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.8 KB (493807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d6288f7dc1449a8dcd11c70cfed803fd2cabd1ebd6026ef3a1b19f247d923da`

```dockerfile
```

-	Layers:
	-	`sha256:f711e56a42f0574e362e02ebbab99fcb0a64759136c0e6a9896f7b5b38dfc25f`  
		Last Modified: Thu, 03 Oct 2024 01:27:03 GMT  
		Size: 463.2 KB (463171 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f32e1ecf6682c808e5973fbe829827f666ccf25b5f93d788d0f85becbd7bdfa`  
		Last Modified: Thu, 03 Oct 2024 01:27:02 GMT  
		Size: 30.6 KB (30636 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:ecbdae30d6cfa95e041cdd386055199ff8d4d416f614a316146c9a16aa37ecc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5454659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cec2dc07b65cb4d183c575c676c85e4746169a30f9cac98d9acf546ab99d0609`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 06 Sep 2024 22:48:17 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
# Fri, 06 Sep 2024 22:48:17 GMT
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b247cb9ed3c8447d6fb9374b7759acc2f7db1b84c2cbe44dd26d2b80b721a71`  
		Last Modified: Thu, 03 Oct 2024 01:35:13 GMT  
		Size: 2.0 MB (1988462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de2ddc0c911294435f1b4f2eecaedfd2590233e9bdf585498a8b195b59cce805`  
		Last Modified: Thu, 03 Oct 2024 01:35:13 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8a0da36e6c51aef0aac09b8074a309e2348c54c7e0465cfdcba3c0518f48bbf`  
		Last Modified: Thu, 03 Oct 2024 01:35:13 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a6f46ef0472a2cb9e23c2d3ecc488bf9111af012c0abc9a9add5a3001bb1d16`  
		Last Modified: Thu, 03 Oct 2024 01:35:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f3e41440c8b36024580a98f0ade46a832f4f450a67f739d20adfe93dbc8b1d`  
		Last Modified: Thu, 03 Oct 2024 01:35:14 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d642f96f3a52f67170412edf5b67d613e852a6bfa41b0c7b1c72f51a73bd84`  
		Last Modified: Thu, 03 Oct 2024 01:35:14 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9e3170d542ed8f2b4f5f417ac3c060ccc742972e653f7967594a1213d824b6b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.7 KB (493663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c763a74315735eeac16b3e0040ea61c02772d5f8e0a061ecc314f2cfd105bda2`

```dockerfile
```

-	Layers:
	-	`sha256:23e4620ab891df228c288cc43c1ab235a1676721001c357df1cd5c54063fc160`  
		Last Modified: Thu, 03 Oct 2024 01:35:13 GMT  
		Size: 463.1 KB (463101 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5c94a30d05af988bc51713492c7d70fe9a503926b18f9c9a8ca24a528fdbe78`  
		Last Modified: Thu, 03 Oct 2024 01:35:13 GMT  
		Size: 30.6 KB (30562 bytes)  
		MIME: application/vnd.in-toto+json
