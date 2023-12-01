## `nginx:alpine-slim`

```console
$ docker pull nginx@sha256:7b875b9d087d3c4ad75eb208354f6298d6b6b915b5bec53e23c2fde16432d92c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `nginx:alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:e3dd8f3abfcc0450c96d61b58c3e05b3b4fdeb0680c155aa3246f9be4b80343a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7371289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab7c6a6862efb5b590cf30c8e775932fea8d636085f035da206fa28a2e859e85`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 02:42:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 Oct 2023 01:22:05 GMT
ENV NGINX_VERSION=1.25.3
# Wed, 25 Oct 2023 01:22:05 GMT
ENV PKG_RELEASE=1
# Wed, 25 Oct 2023 01:22:10 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"00b217979265cc9d66c991c9c89427558936dbaa568d175ca45780589171d94f1866217be09a83438d95494cf38baaa6788320f6d8d23f2fb29c03117391ff88 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 Oct 2023 01:22:10 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 25 Oct 2023 01:22:11 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:22:11 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:22:11 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:22:11 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:22:11 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Oct 2023 01:22:11 GMT
EXPOSE 80
# Wed, 25 Oct 2023 01:22:11 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Oct 2023 01:22:11 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740091335c742882a72f93c12141a4664bcc078b1fc4369e0eea4ceab7dd93ee`  
		Last Modified: Wed, 25 Oct 2023 01:24:41 GMT  
		Size: 4.0 MB (3964756 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da9c2e764c5b41e0bbfc9eb73ac5b2b59da2bdf783bd922fc0bd03619eec5377`  
		Last Modified: Wed, 25 Oct 2023 01:24:38 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ade17ad21ef4248e95654886a2cb2156dec3e40862e33ecc7d8ef64cee3c8a9b`  
		Last Modified: Wed, 25 Oct 2023 01:24:39 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e6f462c8a6979f3030c3fb412b6005166b4d9eb30c8ef00d5b5758399d9d5cf`  
		Last Modified: Wed, 25 Oct 2023 01:24:39 GMT  
		Size: 369.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1324d9977cd29dcc7f79727f27e22624a72074183dff494ca95d1248ae726f77`  
		Last Modified: Wed, 25 Oct 2023 01:24:39 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b9b96da2c74ef457a717b7c55c425ba4a57827d50ccec68105b79c0786a54a4`  
		Last Modified: Wed, 25 Oct 2023 01:24:39 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:763892798daf1ac6ade84433fdd561a1439bdb9c484adc2295a028c06e854a2e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.2 MB (5182792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b983ccdfc57d5d49a3367fd59e8696117c41bcab446fffb742570e26e097cb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:18 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Thu, 30 Nov 2023 22:49:18 GMT
CMD ["/bin/sh"]
# Thu, 30 Nov 2023 23:05:29 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 30 Nov 2023 23:05:29 GMT
ENV NGINX_VERSION=1.25.3
# Thu, 30 Nov 2023 23:05:29 GMT
ENV PKG_RELEASE=1
# Thu, 30 Nov 2023 23:06:26 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"00b217979265cc9d66c991c9c89427558936dbaa568d175ca45780589171d94f1866217be09a83438d95494cf38baaa6788320f6d8d23f2fb29c03117391ff88 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Thu, 30 Nov 2023 23:06:26 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Thu, 30 Nov 2023 23:06:26 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Thu, 30 Nov 2023 23:06:26 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Thu, 30 Nov 2023 23:06:27 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Thu, 30 Nov 2023 23:06:27 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Thu, 30 Nov 2023 23:06:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 30 Nov 2023 23:06:27 GMT
EXPOSE 80
# Thu, 30 Nov 2023 23:06:27 GMT
STOPSIGNAL SIGQUIT
# Thu, 30 Nov 2023 23:06:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f8e205322839aecd038b896e1f24512426ce5b02f51a1b8d7f5511587bd461`  
		Last Modified: Thu, 30 Nov 2023 23:13:10 GMT  
		Size: 2.0 MB (2031343 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e756b6430540a0a9a101a0909a9e735dcadd7193a0f5053d9b4e47e3304934a1`  
		Last Modified: Thu, 30 Nov 2023 23:13:07 GMT  
		Size: 627.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e537369690480a5f7648af9481422d1b8be6547ad2df4afdb9e01048c0374ae`  
		Last Modified: Thu, 30 Nov 2023 23:13:07 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff86a207cc00764dbf2e7297f17205acda868f821927cd7ea65579c84b17417`  
		Last Modified: Thu, 30 Nov 2023 23:13:07 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:577953107dea7127224aa278fb41f692fb3fe4cc186ca108fde439931bf8dd10`  
		Last Modified: Thu, 30 Nov 2023 23:13:07 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8964701224e768317a06b037f56dc09bebceb811f3f003d1c564f62ec8d4ff`  
		Last Modified: Thu, 30 Nov 2023 23:13:07 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:2eaefb28f719ae19df3c4fd404b6f6c82a069c6af2f77efab96b2169d898d297
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.8 MB (6765436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ed3f1a4507c19ccb1ac05cdf6a9a35c9b1cc39629faedcb84ac72e213bafe73`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:56:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 Oct 2023 01:03:28 GMT
ENV NGINX_VERSION=1.25.3
# Wed, 25 Oct 2023 01:03:28 GMT
ENV PKG_RELEASE=1
# Wed, 25 Oct 2023 01:04:13 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"00b217979265cc9d66c991c9c89427558936dbaa568d175ca45780589171d94f1866217be09a83438d95494cf38baaa6788320f6d8d23f2fb29c03117391ff88 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 Oct 2023 01:04:13 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 25 Oct 2023 01:04:13 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:04:13 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:04:13 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:04:13 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:04:13 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Oct 2023 01:04:14 GMT
EXPOSE 80
# Wed, 25 Oct 2023 01:04:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Oct 2023 01:04:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a84711ce23bbebd6c9fbbf4900598e34368607e0b188be46bac70b563dd2f9a`  
		Last Modified: Wed, 25 Oct 2023 01:08:33 GMT  
		Size: 3.9 MB (3860953 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc8ae0fcf20539cbdededc17193e469fae7dcb70c33e271fcfc351258f95366`  
		Last Modified: Wed, 25 Oct 2023 01:08:31 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31f825516df1215e20f854af5fc9e6df8626bef15fc0a0ab5ea3d05cd1522451`  
		Last Modified: Wed, 25 Oct 2023 01:08:30 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1c08069dd09003ba256f81c0e6fea1548a925787f9a2b2868a8665d0f79168a`  
		Last Modified: Wed, 25 Oct 2023 01:08:31 GMT  
		Size: 371.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b4809636aa430add887cd3ae9eb22fe46449457128bcb648afa84113f99d8e1`  
		Last Modified: Wed, 25 Oct 2023 01:08:31 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9411aeaf44cd0002d15e47376c1897db1b0abce4693aecc975d4ae75b88ad89e`  
		Last Modified: Wed, 25 Oct 2023 01:08:31 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:010e53362a161db3a51bde36b42de760cf050542b8a639cb6c7dde891f65a564
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.3 MB (5264796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:436153bee7bff802c9567471dcd8f6b796c0e48299b14dd3d5ad1dc6a16b9eb7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:03 GMT
ADD file:d8a30995bbcd627f084912c728fda5483b6ba486de25af588a0956069d0bd7ad in / 
# Thu, 30 Nov 2023 23:11:03 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 02:40:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 01 Dec 2023 02:40:14 GMT
ENV NGINX_VERSION=1.25.3
# Fri, 01 Dec 2023 02:40:14 GMT
ENV PKG_RELEASE=1
# Fri, 01 Dec 2023 02:40:19 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"00b217979265cc9d66c991c9c89427558936dbaa568d175ca45780589171d94f1866217be09a83438d95494cf38baaa6788320f6d8d23f2fb29c03117391ff88 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 01 Dec 2023 02:40:19 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Fri, 01 Dec 2023 02:40:19 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Fri, 01 Dec 2023 02:40:19 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Fri, 01 Dec 2023 02:40:19 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Fri, 01 Dec 2023 02:40:19 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Fri, 01 Dec 2023 02:40:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 01 Dec 2023 02:40:20 GMT
EXPOSE 80
# Fri, 01 Dec 2023 02:40:20 GMT
STOPSIGNAL SIGQUIT
# Fri, 01 Dec 2023 02:40:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2c03dbb20264f09924f9eab176da44e5421e74a78b09531d3c63448a7baa7c59`  
		Last Modified: Thu, 30 Nov 2023 23:11:32 GMT  
		Size: 3.3 MB (3333033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9250f75ee52732272e435604d91fd0e52ed39048684882ae9ee2afe08b3407aa`  
		Last Modified: Fri, 01 Dec 2023 02:41:38 GMT  
		Size: 1.9 MB (1927185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29521ceb85835c4e79cd486b7edbac4207eba87eea02727da8ae31b60efb2a8f`  
		Last Modified: Fri, 01 Dec 2023 02:41:36 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c14709558ecd5271929fb3ff65f5d996d4e17f01cba4e15c4e85e7fe15e7fe0c`  
		Last Modified: Fri, 01 Dec 2023 02:41:36 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58a34759c9b72ea8cf13d1cdcf7fc5b7a94f27a5b5bd006ab70f0dfe1df76d95`  
		Last Modified: Fri, 01 Dec 2023 02:41:36 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:480fb4b12f42c6d0f93a92c89f8a91e2ec48c5259ec23621835c11d5a20b7482`  
		Last Modified: Fri, 01 Dec 2023 02:41:36 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:379d33e271779a2d32a714570b48ecf9d87bae31a4c8adc8dca4df6109383b11`  
		Last Modified: Fri, 01 Dec 2023 02:41:36 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:97fa474cde5fb31df3683158134712c666bbff1b0c14c09034fefd56fbc55dca
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7636305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2938c620506c163c8837e99db2fad530e1420a779145859f3260bcb452989a24`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 28 Sep 2023 20:38:19 GMT
ADD file:8402753f294e403e92353bd65c86a6428c960be5116c0a15484b663a84f66fcd in / 
# Thu, 28 Sep 2023 20:38:20 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 01:15:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 Oct 2023 00:45:16 GMT
ENV NGINX_VERSION=1.25.3
# Wed, 25 Oct 2023 00:45:16 GMT
ENV PKG_RELEASE=1
# Wed, 25 Oct 2023 00:47:02 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"00b217979265cc9d66c991c9c89427558936dbaa568d175ca45780589171d94f1866217be09a83438d95494cf38baaa6788320f6d8d23f2fb29c03117391ff88 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 Oct 2023 00:47:02 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 25 Oct 2023 00:47:02 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 00:47:02 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 00:47:03 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 00:47:03 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 00:47:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Oct 2023 00:47:03 GMT
EXPOSE 80
# Wed, 25 Oct 2023 00:47:03 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Oct 2023 00:47:03 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:dc95107ad2a031a015320bb397f73ec151d738127175b31ad643120697dc7e90`  
		Last Modified: Thu, 28 Sep 2023 20:39:32 GMT  
		Size: 3.2 MB (3235757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942218e7c1efefbf0e180fc1747b971392ad9422c19ed5c518c4183145810d08`  
		Last Modified: Wed, 25 Oct 2023 00:52:24 GMT  
		Size: 4.4 MB (4395970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b53cec1f9fdc9b7ffd3f8a75f6b994470e5479aa071659090a12a659dc28e8f`  
		Last Modified: Wed, 25 Oct 2023 00:52:21 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2adf5aa94f5b821713594373f2a28d71766865ce61a569ae78b0b83eec581a7e`  
		Last Modified: Wed, 25 Oct 2023 00:52:21 GMT  
		Size: 958.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dba2e16ebb457cb660089e0302fd3d76268f3fb537c9f37e45d511290664ce0`  
		Last Modified: Wed, 25 Oct 2023 00:52:21 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7455815fa3363d35d504c5670840577108102f749f5fc08b14b08352db7b6ed1`  
		Last Modified: Wed, 25 Oct 2023 00:52:21 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85c64e91136c486ce2334a8b89ebd1669aae804cee2c659315ceb53a7a6bcaae`  
		Last Modified: Wed, 25 Oct 2023 00:52:21 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:554732ff75b075adce1c766623f22ded3d0f6df295b898bf0bc3328a8059e7c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.8 MB (7799036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb4c7f2a7af4d929896a70d6c10f40dee1a71f293b5d21c518b625cd832b2d4c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 28 Sep 2023 21:22:20 GMT
ADD file:a720acb99214334c501363d564d8cae9b90d062ccf8a24a5ba1c831545b783dd in / 
# Thu, 28 Sep 2023 21:22:21 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:39:00 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 Oct 2023 01:28:59 GMT
ENV NGINX_VERSION=1.25.3
# Wed, 25 Oct 2023 01:28:59 GMT
ENV PKG_RELEASE=1
# Wed, 25 Oct 2023 01:29:50 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"00b217979265cc9d66c991c9c89427558936dbaa568d175ca45780589171d94f1866217be09a83438d95494cf38baaa6788320f6d8d23f2fb29c03117391ff88 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 Oct 2023 01:29:50 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 25 Oct 2023 01:29:50 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:29:51 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:29:51 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:29:51 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 01:29:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Oct 2023 01:29:52 GMT
EXPOSE 80
# Wed, 25 Oct 2023 01:29:54 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Oct 2023 01:29:54 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:cd37f9856024d6685ac0233823aded690551c5872d6a27699a96c6a479d20f6f`  
		Last Modified: Thu, 28 Sep 2023 21:23:43 GMT  
		Size: 3.3 MB (3346508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5783b182504ca0f33494f2ebfeccd7f3a4f296862c88c6109d8cc3dbe5011205`  
		Last Modified: Wed, 25 Oct 2023 01:36:47 GMT  
		Size: 4.4 MB (4447948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4181207dc75994d62e33950e825ded30da4a9fb64c2ef0d683914ea365a3c413`  
		Last Modified: Wed, 25 Oct 2023 01:36:44 GMT  
		Size: 628.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdfcde034573c0eda5c8accfa204fd7bfb1828682c0c4d6b0a72ffa6351e0082`  
		Last Modified: Wed, 25 Oct 2023 01:36:44 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:924f15c3ba0650ff64605a126c5e0bf1c6e2285158be91a762fbcbc585982819`  
		Last Modified: Wed, 25 Oct 2023 01:36:44 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:446a1e7794349489702e03de5d2ac1c8d6f19930ce2d7e1d2286afc9732b5de8`  
		Last Modified: Wed, 25 Oct 2023 01:36:44 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4ac002269126c1b6b75c993b2a13448ccf606af30e36625bedf347a8f8e6eee`  
		Last Modified: Wed, 25 Oct 2023 01:36:44 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:66e9926dd1efeaebf7726b8c5982130c457f929f45d4dd1d3839ffc8169ccc8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7525667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6955cfcb02919c68f0ec8d10f7d1f44a5c3624a68612bb79648378f51a3bbcc0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 28 Sep 2023 20:41:43 GMT
ADD file:fd3808a676fc56c1380e55b2ddbf4014d9371346cf789860b336bc9f00729ed0 in / 
# Thu, 28 Sep 2023 20:41:44 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 00:35:34 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 Oct 2023 00:50:44 GMT
ENV NGINX_VERSION=1.25.3
# Wed, 25 Oct 2023 00:50:44 GMT
ENV PKG_RELEASE=1
# Wed, 25 Oct 2023 00:51:43 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"00b217979265cc9d66c991c9c89427558936dbaa568d175ca45780589171d94f1866217be09a83438d95494cf38baaa6788320f6d8d23f2fb29c03117391ff88 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 25 Oct 2023 00:51:43 GMT
COPY file:01e75c6dd0ce317d516928a17584d111cd082840c01e58be0afc851b33adb916 in / 
# Wed, 25 Oct 2023 00:51:44 GMT
COPY file:caec368f5a54f70a844a13005eb2255bed778809b3672d516e719ce2f4bce123 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 00:51:44 GMT
COPY file:3b1b9915b7dd898a0e32f7eb9715a35c9feab914022efff68ba990bc1ec7d169 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 00:51:45 GMT
COPY file:57846632accc89753f45cbc00cb9e6223d991e1d31297eec3395a7ca58eed6a6 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 00:51:45 GMT
COPY file:9e3b2b63db9f8fc702e2dc2bdd0943be0d990c028cddcf1c159f5556a8ba3030 in /docker-entrypoint.d 
# Wed, 25 Oct 2023 00:51:46 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Oct 2023 00:51:47 GMT
EXPOSE 80
# Wed, 25 Oct 2023 00:51:47 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Oct 2023 00:51:48 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:47539bffe0f44273ec7731d86be2a6171359b3847c9b60c6ac74c4875c3264af`  
		Last Modified: Thu, 28 Sep 2023 20:43:18 GMT  
		Size: 3.2 MB (3215103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa13faf508082d62c9ef393d42e7d9895ab7b7e4e2a969bde43f693b904cdca9`  
		Last Modified: Wed, 25 Oct 2023 00:58:46 GMT  
		Size: 4.3 MB (4305986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8652d1909bb3d44d77f6e9e65820eb4998f1ab995f9009be47514d5a095e6169`  
		Last Modified: Wed, 25 Oct 2023 00:58:44 GMT  
		Size: 626.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d61f3b0cb018b7015150f4fef43a2c974efc4998533f5839283f40c050fb636`  
		Last Modified: Wed, 25 Oct 2023 00:58:43 GMT  
		Size: 959.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5466f3b823269a04cf0fd548f37489fdb165531404f36519e43332523b36807`  
		Last Modified: Wed, 25 Oct 2023 00:58:44 GMT  
		Size: 372.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4be5fb67c53dd2da159cd6c4020e5edc724e999995a6f5b415548886ff46d2fe`  
		Last Modified: Wed, 25 Oct 2023 00:58:44 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bdc6cbfd1ac30f8b0f6a4655e170c0ea1ec214964d112c0541721b851cfaa94`  
		Last Modified: Wed, 25 Oct 2023 00:58:43 GMT  
		Size: 1.4 KB (1405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
