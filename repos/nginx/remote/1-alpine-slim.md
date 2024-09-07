## `nginx:1-alpine-slim`

```console
$ docker pull nginx@sha256:f4064ca274f356bf19daff5d336dbcf825b11c313aa560d5be401785eb13f8ee
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
$ docker pull nginx@sha256:784b266cc772718bb9a9cb2e5516a5673423b906f5779ede310beec1885a5a96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.8 MB (4824493 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c90047bf1d1747984dc3b6cc392f5bebf7114f13e4f80398a12a0c2816b66fcc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:8096a7e97160f837a432988b8138ffab07ff212be781f530c8baa2067265d071 in / 
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
	-	`sha256:da2748c71804914f58a58693c998a4885dd24623380daf301f4a1a88185cb4c8`  
		Last Modified: Fri, 06 Sep 2024 22:08:26 GMT  
		Size: 3.1 MB (3095502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e1d94272643975401de3b560557a560ade1ad9eae18c9eb21ac96cdec5e22d1`  
		Last Modified: Sat, 07 Sep 2024 03:00:16 GMT  
		Size: 1.7 MB (1724401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff39f272c45c31a02658052537bd38808d5a71c04a6bc7d38b3de1fba01b7940`  
		Last Modified: Sat, 07 Sep 2024 03:00:16 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edf0eb3319375ff3433348d2c3ee923d99a8bfd89e96d8b7f7486881f013ebc`  
		Last Modified: Sat, 07 Sep 2024 03:00:16 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67178cb42b4ce056773d0c5546d1886e6dc717b9cf5087c99e6c2f8a61bbf3cf`  
		Last Modified: Sat, 07 Sep 2024 03:00:16 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d2850ffda776ce5a42389ace008b321b5cf078422be951ef7995671592ce3`  
		Last Modified: Sat, 07 Sep 2024 03:00:17 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:931d35683bbf7b06c3dea5c4167413f66cd95a7f38e304476bc21f448063ebda`  
		Last Modified: Sat, 07 Sep 2024 03:00:17 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:5d58d5a4a4245a02c95062f62d2b1029bd1339387153de8579ede43e39f374f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.8 KB (495782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b07882c86843057302956eff09db69b234b27781def6d15d66089bd45989f63`

```dockerfile
```

-	Layers:
	-	`sha256:42d14a068b6e6d68bd57a1825752a3780253a2e7dc8ee6bafed9e08fc211b331`  
		Last Modified: Sat, 07 Sep 2024 03:00:16 GMT  
		Size: 465.1 KB (465126 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88a61a951576905e3bef03c2512c63fd14a4b157fd50dd9b237a33941fd7e08e`  
		Last Modified: Sat, 07 Sep 2024 03:00:16 GMT  
		Size: 30.7 KB (30656 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:721cb3c63c0e47b5c5651431964225df6b15560094ef6e1b0885cbab1b120fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 MB (5879146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4bdeead39f8ec936a137d0de2704e18ba539e2f806154f389dc002ce4c6abd3b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:ee5bb8409915b11413f44cce4c22fed658aba4fb078a448e08dd4ac9a23581f2 in / 
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
	-	`sha256:cf04c63912e16506c4413937c7f4579018e4bb25c272d989789cfba77b12f951`  
		Last Modified: Fri, 06 Sep 2024 22:44:39 GMT  
		Size: 4.1 MB (4087646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af676cbe1eebad012784df0b450beb143af153514b61986d262cfae62f83335d`  
		Last Modified: Sat, 07 Sep 2024 05:31:05 GMT  
		Size: 1.8 MB (1786914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bd499aae1693a481ec5f38cefa5f8803e0d8a5bef0c20cb3e6989eb2975cde9`  
		Last Modified: Sat, 07 Sep 2024 05:31:04 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a258ad06a688beff3d4a30eede1b350e64a9ebbd5b80b8a095eec17f3f5a9e15`  
		Last Modified: Sat, 07 Sep 2024 05:31:04 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906b4c822d155ab6595749cb264093152af7faafabdc0d5534fb161909cf71b4`  
		Last Modified: Sat, 07 Sep 2024 05:31:04 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:780210e97849521bfdd49e752a71a1e150219ee398e1bd8c6399e7d8797b923f`  
		Last Modified: Sat, 07 Sep 2024 05:31:05 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45d5bc49ce25a46e0fa4f1481ae38f289d8f5f6b207ff03d038bcb784afe821e`  
		Last Modified: Sat, 07 Sep 2024 05:31:05 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:7a58b8a16c1193ba7d8f0981635699371415b9c9f7c53ea6bad1cae556a7b810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **496.1 KB (496080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8bd3d814866f574f5f5be6f1a78ec84129c362fb4a24c99ff3460ec6b4a9442`

```dockerfile
```

-	Layers:
	-	`sha256:10eabbc13cb72e38dffaf27afa1b6dadd111de0d29fac71dfb4effbe3b8ae340`  
		Last Modified: Sat, 07 Sep 2024 05:31:04 GMT  
		Size: 465.2 KB (465170 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c857f73d8ce4cd118f95c370ac1afddaefffbf2940efc10090c156381a57c213`  
		Last Modified: Sat, 07 Sep 2024 05:31:04 GMT  
		Size: 30.9 KB (30910 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:a3e79782502a442c2d1f0b05557f52c1b2b332cb9dbf1cf405214f1bf6126988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5432980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1fa0859041ba9c86972bb0e96932df068f7ca20232cfefba50374acb0b4b447`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:00e6c22c1917031dd97c411814ae384c25a7f2bb91890494a73ea34f3c168453 in / 
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
	-	`sha256:2689ac6c14fd48d5dbd1df1dd2d317f177e131f689c1a010922edcd778518efd`  
		Last Modified: Fri, 06 Sep 2024 22:41:47 GMT  
		Size: 3.5 MB (3469165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1855221e7a1ad96fc4dac601e00f56ed5d332465b153791b5288749baf365311`  
		Last Modified: Fri, 06 Sep 2024 23:23:31 GMT  
		Size: 2.0 MB (1959230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d37a25ecfba36e81b25f8b7b80bb0bbdd33d58086d14f9c2f44a100a880509`  
		Last Modified: Fri, 06 Sep 2024 23:23:31 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:498a89ebf32db6a45d88d2bb81d82213af865e89bb546e980e68c96e98aa8c2c`  
		Last Modified: Fri, 06 Sep 2024 23:23:31 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6271a2e23dc16a3852e1e6d244cb222a42c81ea0a760c29e7f1238b35ba5935`  
		Last Modified: Fri, 06 Sep 2024 23:23:31 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ab859dad20a95d40169714ca90ae70f30e3a43386e1096197252a0a95dc5c7`  
		Last Modified: Fri, 06 Sep 2024 23:23:32 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19a8a010e954b22d8bfe8f1ac9d2b638c2babac9f7d541dfd004ce9e26d9cc71`  
		Last Modified: Fri, 06 Sep 2024 23:23:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c1aa62fac9314ba8aeda8f8e6d896dfe43e041db95d1f4b80317144330ca5c37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **495.5 KB (495465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67fa351cffc4ff5fdd7b174f0463d47a82e55fdf8e9c8b9c246061a77f4aac9`

```dockerfile
```

-	Layers:
	-	`sha256:eeb9d7fbcf3cf559224f26f9084372aea00651f6631252cac0ea4a26e97cb7d2`  
		Last Modified: Fri, 06 Sep 2024 23:23:31 GMT  
		Size: 465.0 KB (464987 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfc045fa772f41d45d913b09c3b29f01b7b70e77953b7ad4d0b3de3966ab46d8`  
		Last Modified: Fri, 06 Sep 2024 23:23:31 GMT  
		Size: 30.5 KB (30478 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:e73b7b9401091653f076eb2770483271b2e5a108c32e4c5f60a721ed9708a3a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.5 MB (5530305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee606f93e80b61b08a8496af332616eed7539f6f7445a8968644c5e6604f44a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 22 Jul 2024 21:26:21 GMT
ADD file:9fcad21b83b7efd6ef267ba714c3ef5a8d4d2064a0bdf528cbb17d0c3388f03f in / 
# Mon, 22 Jul 2024 21:26:22 GMT
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
	-	`sha256:6e59b4988c495782a5b0c8f8d6698931851c16c5c0fc5ef09cbb0637ade56e36`  
		Last Modified: Mon, 22 Jul 2024 21:26:52 GMT  
		Size: 3.6 MB (3571555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20b53e18dc6a0564b58eaea94868b4a88d6f32ed8d402b620e7602cca7b4ff5d`  
		Last Modified: Thu, 15 Aug 2024 18:50:30 GMT  
		Size: 2.0 MB (1954157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb34f7f10a490a8748d693a4f9dcb9c944cfd6a24a6c7a5b7f68eb6de181a829`  
		Last Modified: Thu, 15 Aug 2024 18:50:29 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12ab181482faf279979c3ac2b46c0262f3af289af39a3bb51f0c6cae35f5c6f2`  
		Last Modified: Thu, 15 Aug 2024 18:50:29 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c19885827a3dbe17ea5c340a90e970066607474d7e73013469f46237cfc9f330`  
		Last Modified: Thu, 15 Aug 2024 18:50:29 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bbefd6cbb1fffe2cd5067b2cdcf8073a77a9b6bbbb637ae405023842ec7551f`  
		Last Modified: Thu, 15 Aug 2024 18:50:30 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abff9d09bd665c93218d427f9e192a605fd9ef41c1f38b9e43b154faf7f681f4`  
		Last Modified: Thu, 15 Aug 2024 18:50:30 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:fc95c2f28e739808373fcadb2c6740ad153283a61a8aee53bb0d6764a4a937ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.8 KB (493770 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0d8b75178e6926baa6969e45897f043fa1d758e9de9f524c2c80d99c3a60e46`

```dockerfile
```

-	Layers:
	-	`sha256:e50a99d34986cc5b48cc9466faafab36f3aa80671ec7e698f66f1930de7d96cb`  
		Last Modified: Thu, 15 Aug 2024 18:50:29 GMT  
		Size: 463.2 KB (463158 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:658d540b78d93479e7c6b4d9a9e5d1a937719b4dfc5fc36c5f3c64c65d1eec6b`  
		Last Modified: Thu, 15 Aug 2024 18:50:29 GMT  
		Size: 30.6 KB (30612 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:2c68f8191ce5f7d4ada19c2c50a2196b74cc8caaed68f284da9277ac6075b6ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5445165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28f80afee76cd10a3900c6baf91745aed26460ac0d59b64bf1cc33e8c78379d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 23:51:24 GMT
ADD file:ba2637314e600db5a647501cf1ab287c5f51de1627c13bc1d82aa48925a3dd78 in / 
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
	-	`sha256:df110db6acd600b9ee5ebd7b510779652f96424d3f80321a4e0dcb8a09aa0526`  
		Last Modified: Fri, 06 Sep 2024 22:48:57 GMT  
		Size: 3.5 MB (3461598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:637ea86e0775eda18d777873e3329c11e89cfc8dd2797065481e87252d12fbfd`  
		Last Modified: Sat, 07 Sep 2024 02:53:05 GMT  
		Size: 2.0 MB (1978970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c01d83c29f0d7c087fdb311c320710d4b3c833850a862a0ec59f23ea1b0a1506`  
		Last Modified: Sat, 07 Sep 2024 02:53:05 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c72540907a63d668c1504c88158c7cfa68092d3ace767dd699a21014de9ee6e`  
		Last Modified: Sat, 07 Sep 2024 02:53:05 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de5eb8bef99d90facc374d8e10d0ece4b07459bda6d8dc50d2924f009d53057b`  
		Last Modified: Sat, 07 Sep 2024 02:53:05 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6503fb042a25b5e4e8cedca3ca6c4ba539b87534697f60528509a34fe9fa401`  
		Last Modified: Sat, 07 Sep 2024 02:53:06 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93b43b1ee457d999d422fa03413668d26bfda5152e4e69e27f1dc6515bbb37b`  
		Last Modified: Sat, 07 Sep 2024 02:53:06 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b27d308bffb4969fb590ce60c283fb8decbe5fe950311a2879103c6bbf310a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **493.6 KB (493626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c458819b6407aa43ca1ed2e9b6373b1556f515008779542932d01dd5eafc4d8`

```dockerfile
```

-	Layers:
	-	`sha256:258973c41badecbe3bd34f4631680e34bda4ddb4d03f4de62af3de7d6961932a`  
		Last Modified: Sat, 07 Sep 2024 02:53:05 GMT  
		Size: 463.1 KB (463088 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0a8dd79a9b81450c944b749ac46397aff04f4355d9af1b3f5016ed62f6bbcd`  
		Last Modified: Sat, 07 Sep 2024 02:53:06 GMT  
		Size: 30.5 KB (30538 bytes)  
		MIME: application/vnd.in-toto+json
