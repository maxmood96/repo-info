## `nginx:stable-alpine`

```console
$ docker pull nginx@sha256:56824cdebbc1c79143b6f20b839576595bf21e2feda3c78cce4a0a285a8c50ad
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

### `nginx:stable-alpine` - linux; amd64

```console
$ docker pull nginx@sha256:1aeb5626e29b4f463ce25fc4b07c85eb231f50494d2f46d9184153a4e938302e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.2 MB (10189262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccb911fdd2ca863fc63c48b9d91a4637e104e153bce97ff38135937b3e2c273d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:43:27 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 18 Jul 2022 23:43:54 GMT
ENV NGINX_VERSION=1.22.0
# Tue, 19 Jul 2022 19:21:50 GMT
ENV NJS_VERSION=0.7.6
# Tue, 19 Jul 2022 19:21:50 GMT
ENV PKG_RELEASE=1
# Tue, 19 Jul 2022 19:21:57 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/725.tar.gz                 && PKGOSSCHECKSUM=\"a6c56bb7e98be77337affe349e1316a71ddad7a732dc3b34294a794b3e740d68385022f0de72d08c090156f194580a92dcb8b5e2aa1c9c29b5a8484a6431e9b3 *725.tar.gz\"                 && if [ \"\$(openssl sha512 -r 725.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 725.tar.gz                 && cd pkg-oss-725                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 19 Jul 2022 19:21:57 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 19 Jul 2022 19:21:57 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:21:57 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:21:57 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:21:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 19:21:57 GMT
EXPOSE 80
# Tue, 19 Jul 2022 19:21:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 19:21:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d68eaa7f9bef26d3fb2db7037984deb50990b661bbb9488647e3703933695be`  
		Last Modified: Tue, 19 Jul 2022 19:24:41 GMT  
		Size: 7.4 MB (7386903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9841618ceff92df33ec8689bc087d3d61a8e35aca3c06bd6e83dfc8c78901b26`  
		Last Modified: Tue, 19 Jul 2022 19:24:40 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69fca60111637993463346cba631527119af5a2b8c2dfca9f4c7b2641913bfed`  
		Last Modified: Tue, 19 Jul 2022 19:24:40 GMT  
		Size: 893.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44d90e8630229289df923c6998dc778489b12c659de7dd9f653a8e7dc69e2b74`  
		Last Modified: Tue, 19 Jul 2022 19:24:40 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6fa4ee325c30e8280915d48a8970a2a81f7312436746fd01dbc41f4efd8794`  
		Last Modified: Tue, 19 Jul 2022 19:24:40 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-alpine` - linux; arm variant v6

```console
$ docker pull nginx@sha256:04ac9903aaa19ff07014e3bef80e045fb8a7730ffda45b82566a83eb2276593b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.7 MB (9689177 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2c53139cf79b6990a84a8fe974d4dcdd864e96b5902d0176883f548a2b0d633`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 01:08:03 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 Jul 2022 01:24:12 GMT
ENV NGINX_VERSION=1.22.0
# Tue, 19 Jul 2022 19:05:41 GMT
ENV NJS_VERSION=0.7.6
# Tue, 19 Jul 2022 19:05:42 GMT
ENV PKG_RELEASE=1
# Tue, 19 Jul 2022 19:13:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/725.tar.gz                 && PKGOSSCHECKSUM=\"a6c56bb7e98be77337affe349e1316a71ddad7a732dc3b34294a794b3e740d68385022f0de72d08c090156f194580a92dcb8b5e2aa1c9c29b5a8484a6431e9b3 *725.tar.gz\"                 && if [ \"\$(openssl sha512 -r 725.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 725.tar.gz                 && cd pkg-oss-725                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 19 Jul 2022 19:13:08 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 19 Jul 2022 19:13:09 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:13:09 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:13:10 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:13:10 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 19:13:11 GMT
EXPOSE 80
# Tue, 19 Jul 2022 19:13:11 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 19:13:12 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c36e0457f79e51a6de6f3b8d5f0287e7a8b1c0c33acc67c2c243c8899fef06`  
		Last Modified: Tue, 19 Jul 2022 19:23:29 GMT  
		Size: 7.1 MB (7079188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:997f35e0e4c5a5bb81e7a0d92beccab3239ded1f3faf520cd6f80033eeaac6e0`  
		Last Modified: Tue, 19 Jul 2022 19:23:25 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93da3e1db6a6238ccb9958a021b6afbd59b193aa4f8348a0282fc6fad4e0c1c`  
		Last Modified: Tue, 19 Jul 2022 19:23:25 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3919fa8871265a71548422e3d79c635c32650d4f75e38c3ebeb12e7a99b6456`  
		Last Modified: Tue, 19 Jul 2022 19:23:25 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a59217e3d8b842d8e504e5f7d18226c3f4bb0413f0969ca94a1e5493348641`  
		Last Modified: Tue, 19 Jul 2022 19:23:25 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-alpine` - linux; arm variant v7

```console
$ docker pull nginx@sha256:1c4a6608366a8039f1bc562c64487ac7dc5cf36971bfccc8af0393c0fa2b46de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8909856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab4190774d4ccf8f948360d1702990cce041b504cfb370d5403b32aebcf6c0db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 03 Aug 2022 20:16:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 03 Aug 2022 20:32:23 GMT
ENV NGINX_VERSION=1.22.0
# Wed, 03 Aug 2022 20:32:23 GMT
ENV NJS_VERSION=0.7.6
# Wed, 03 Aug 2022 20:32:24 GMT
ENV PKG_RELEASE=1
# Wed, 03 Aug 2022 20:36:22 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/725.tar.gz                 && PKGOSSCHECKSUM=\"a6c56bb7e98be77337affe349e1316a71ddad7a732dc3b34294a794b3e740d68385022f0de72d08c090156f194580a92dcb8b5e2aa1c9c29b5a8484a6431e9b3 *725.tar.gz\"                 && if [ \"\$(openssl sha512 -r 725.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 725.tar.gz                 && cd pkg-oss-725                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Wed, 03 Aug 2022 20:36:22 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Wed, 03 Aug 2022 20:36:22 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Wed, 03 Aug 2022 20:36:22 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Wed, 03 Aug 2022 20:36:22 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Wed, 03 Aug 2022 20:36:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 03 Aug 2022 20:36:23 GMT
EXPOSE 80
# Wed, 03 Aug 2022 20:36:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 03 Aug 2022 20:36:23 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a0148c06c9733a05296c274e9e160fe4427f71a2999e6023ee213f09479a71`  
		Last Modified: Wed, 03 Aug 2022 20:44:19 GMT  
		Size: 6.5 MB (6493988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8549c6790cc71c2688dadbf0e8106338757954c5fe7aef04b43ffcd54bbe5175`  
		Last Modified: Wed, 03 Aug 2022 20:44:18 GMT  
		Size: 602.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91c6cb1be5c993e20b72459037c554fd5284c3a2f54c6cfd3f22af480bf90832`  
		Last Modified: Wed, 03 Aug 2022 20:44:18 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:011d6fe31f686acb082d122f8fbd2a012d51f8effdc1301aa8a56d04ead73029`  
		Last Modified: Wed, 03 Aug 2022 20:44:18 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96695200938e12bd3b47076ae4387ab2f9f2068e6157391882b1d4cbe0a0ff4a`  
		Last Modified: Wed, 03 Aug 2022 20:44:18 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-alpine` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:ac8e25727d08186fe33adef63bc6260bb430f9665e7ce656dda147a2d2fa29a6
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.0 MB (9977790 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b85c6f8d1dc2282bea8ac8e3bd59ef31cd8ea0b72090cc8c75ae441ed8aa03fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:46:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 18 Jul 2022 23:47:46 GMT
ENV NGINX_VERSION=1.22.0
# Tue, 19 Jul 2022 18:44:40 GMT
ENV NJS_VERSION=0.7.6
# Tue, 19 Jul 2022 18:44:41 GMT
ENV PKG_RELEASE=1
# Tue, 19 Jul 2022 18:46:38 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/725.tar.gz                 && PKGOSSCHECKSUM=\"a6c56bb7e98be77337affe349e1316a71ddad7a732dc3b34294a794b3e740d68385022f0de72d08c090156f194580a92dcb8b5e2aa1c9c29b5a8484a6431e9b3 *725.tar.gz\"                 && if [ \"\$(openssl sha512 -r 725.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 725.tar.gz                 && cd pkg-oss-725                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 19 Jul 2022 18:46:40 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 19 Jul 2022 18:46:41 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 19 Jul 2022 18:46:42 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 19 Jul 2022 18:46:43 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 19 Jul 2022 18:46:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 18:46:44 GMT
EXPOSE 80
# Tue, 19 Jul 2022 18:46:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 18:46:46 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47b29ee3973f8d063e25793b54caf3dde417b5fd462eea7d1d3ebda11a4898ad`  
		Last Modified: Tue, 19 Jul 2022 18:50:38 GMT  
		Size: 7.3 MB (7279507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cde0c1f08b11afd2fc27fe3478b05cdc4da11898438038a39834245fb57f0795`  
		Last Modified: Tue, 19 Jul 2022 18:50:37 GMT  
		Size: 603.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b6a8e24d3ad6783f66e1f003085121891069be8bf2b6ace652939ef303393cb`  
		Last Modified: Tue, 19 Jul 2022 18:50:37 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64bbcd6a7ea6bff361ea167d1c1c441995d3baeae9a92a032a28851b2aa54686`  
		Last Modified: Tue, 19 Jul 2022 18:50:37 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c01a54cc3b9703628572848279bdb3c5dd7df59171b49c4594eb6d7386ab390`  
		Last Modified: Tue, 19 Jul 2022 18:50:37 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-alpine` - linux; 386

```console
$ docker pull nginx@sha256:0baef51cb3d4235cfc10b97b62b548d8ad1d14e9060bbcb36657afd7a63d3942
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.7 MB (10693778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c939919503d8539c227694cecfc5ee97dbb676862d017d041ad178de848f663b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 18:38:58 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 09 Aug 2022 18:45:48 GMT
ENV NGINX_VERSION=1.22.0
# Tue, 09 Aug 2022 18:45:49 GMT
ENV NJS_VERSION=0.7.6
# Tue, 09 Aug 2022 18:45:50 GMT
ENV PKG_RELEASE=1
# Tue, 09 Aug 2022 18:48:50 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/725.tar.gz                 && PKGOSSCHECKSUM=\"a6c56bb7e98be77337affe349e1316a71ddad7a732dc3b34294a794b3e740d68385022f0de72d08c090156f194580a92dcb8b5e2aa1c9c29b5a8484a6431e9b3 *725.tar.gz\"                 && if [ \"\$(openssl sha512 -r 725.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 725.tar.gz                 && cd pkg-oss-725                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 09 Aug 2022 18:48:51 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 09 Aug 2022 18:48:52 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 09 Aug 2022 18:48:53 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 09 Aug 2022 18:48:54 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 09 Aug 2022 18:48:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 09 Aug 2022 18:48:55 GMT
EXPOSE 80
# Tue, 09 Aug 2022 18:48:56 GMT
STOPSIGNAL SIGQUIT
# Tue, 09 Aug 2022 18:48:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45c37dc9487031ef650ba0956e15de7a67f9326dda436d8bc890d95575f4090e`  
		Last Modified: Tue, 09 Aug 2022 18:54:31 GMT  
		Size: 7.9 MB (7883096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ddc6789c334952bbf81eb65b293213067dabcd25949ff4f51b0948132888e0`  
		Last Modified: Tue, 09 Aug 2022 18:54:30 GMT  
		Size: 601.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2384581612adff28539e813ae5e03b6dd325f7573d5f1a86f2b8b4e29b2867f`  
		Last Modified: Tue, 09 Aug 2022 18:54:30 GMT  
		Size: 896.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ae12876084694673a5086a07c37fcd9dc02ffef7218babed985242df849f18b`  
		Last Modified: Tue, 09 Aug 2022 18:54:30 GMT  
		Size: 667.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e02350e40ed469b9cada13e06a5549e7b294202354f7eb85cab217f01e729953`  
		Last Modified: Tue, 09 Aug 2022 18:54:30 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-alpine` - linux; ppc64le

```console
$ docker pull nginx@sha256:f7987b9768bec1d020edd0007ec57c09e3353f6a67d856e7ed62c105f3774339
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.5 MB (10502838 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d99ef6e678fe801e23bf0151a244996e767fb279b0714a889321b771244a6aa2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Fri, 29 Jul 2022 16:20:40 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 29 Jul 2022 16:33:05 GMT
ENV NGINX_VERSION=1.22.0
# Fri, 29 Jul 2022 16:33:05 GMT
ENV NJS_VERSION=0.7.6
# Fri, 29 Jul 2022 16:33:05 GMT
ENV PKG_RELEASE=1
# Fri, 29 Jul 2022 16:37:35 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/725.tar.gz                 && PKGOSSCHECKSUM=\"a6c56bb7e98be77337affe349e1316a71ddad7a732dc3b34294a794b3e740d68385022f0de72d08c090156f194580a92dcb8b5e2aa1c9c29b5a8484a6431e9b3 *725.tar.gz\"                 && if [ \"\$(openssl sha512 -r 725.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 725.tar.gz                 && cd pkg-oss-725                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Fri, 29 Jul 2022 16:37:36 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Fri, 29 Jul 2022 16:37:36 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Fri, 29 Jul 2022 16:37:37 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Fri, 29 Jul 2022 16:37:37 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Fri, 29 Jul 2022 16:37:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 29 Jul 2022 16:37:38 GMT
EXPOSE 80
# Fri, 29 Jul 2022 16:37:38 GMT
STOPSIGNAL SIGQUIT
# Fri, 29 Jul 2022 16:37:38 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d3b29a8d552ba0821f9f8cc299e4aa151234b5409e540c28cf7888465483d1b`  
		Last Modified: Fri, 29 Jul 2022 16:44:36 GMT  
		Size: 7.7 MB (7709361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b5ac1e99c60bc92176790b64e45cf9b15bc630590c6e93d853b2b88f8016c0`  
		Last Modified: Fri, 29 Jul 2022 16:44:34 GMT  
		Size: 600.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a84ee19a293d7d8f30c553878c7d47dc0a3bda22bdfdcc180d2eb3c17d24912`  
		Last Modified: Fri, 29 Jul 2022 16:44:34 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:752cb1896976d9991024543b448d6c3740db09ad45235d6d925e2bf047900feb`  
		Last Modified: Fri, 29 Jul 2022 16:44:34 GMT  
		Size: 666.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c51518ef5b456e0676cfde64504b7af4c161a46a8dd0ceb667f74b7fcd120fc`  
		Last Modified: Fri, 29 Jul 2022 16:44:34 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `nginx:stable-alpine` - linux; s390x

```console
$ docker pull nginx@sha256:8fb97e062c361ceee0381259efaf81aa06d24d87c0d0f60a0d47bba77ec5751a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.9 MB (9894698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ca946617fc31efe9e01f495b52c6a63a305fd66de0a646490c754238370c14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 Jul 2022 20:41:35 GMT
ADD file:deaa573cd61e07709846a5300fb627a8610e9754129c085ed483ff8897d0c002 in / 
# Mon, 18 Jul 2022 20:41:36 GMT
CMD ["/bin/sh"]
# Tue, 19 Jul 2022 05:44:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 Jul 2022 05:56:33 GMT
ENV NGINX_VERSION=1.22.0
# Tue, 19 Jul 2022 18:59:59 GMT
ENV NJS_VERSION=0.7.6
# Tue, 19 Jul 2022 18:59:59 GMT
ENV PKG_RELEASE=1
# Tue, 19 Jul 2022 19:05:59 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e7fa8303923d9b95db37a77ad46c68fd4755ff935d0a534d26eba83de193c76166c68bfe7f65471bf8881004ef4aa6df3e34689c305662750c0172fca5d8552a *stdin"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if [ "$(openssl rsa -pubin -in /tmp/nginx_signing.rsa.pub -text -noout | openssl sha512 -r)" = "$KEY_SHA512" ]; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 perl-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/725.tar.gz                 && PKGOSSCHECKSUM=\"a6c56bb7e98be77337affe349e1316a71ddad7a732dc3b34294a794b3e740d68385022f0de72d08c090156f194580a92dcb8b5e2aa1c9c29b5a8484a6431e9b3 *725.tar.gz\"                 && if [ \"\$(openssl sha512 -r 725.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 725.tar.gz                 && cd pkg-oss-725                 && cd alpine                 && make all                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && apk add --no-cache curl ca-certificates     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d
# Tue, 19 Jul 2022 19:06:01 GMT
COPY file:65504f71f5855ca017fb64d502ce873a31b2e0decd75297a8fb0a287f97acf92 in / 
# Tue, 19 Jul 2022 19:06:01 GMT
COPY file:0b866ff3fc1ef5b03c4e6c8c513ae014f691fb05d530257dfffd07035c1b75da in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:06:02 GMT
COPY file:0fd5fca330dcd6a7de297435e32af634f29f7132ed0550d342cad9fd20158258 in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:06:02 GMT
COPY file:09a214a3e07c919af2fb2d7c749ccbc446b8c10eb217366e5a65640ee9edcc25 in /docker-entrypoint.d 
# Tue, 19 Jul 2022 19:06:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 Jul 2022 19:06:03 GMT
EXPOSE 80
# Tue, 19 Jul 2022 19:06:04 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 Jul 2022 19:06:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5f1840d5bacf4162a87f497e22d94bce946e660bdfce8eeefcbf7bd0beb193f3`  
		Last Modified: Mon, 18 Jul 2022 20:42:36 GMT  
		Size: 2.6 MB (2580798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d36cb0ed368dfbae96d32692edcacef57eb1acc8acebaf9358e8b825fc257d0`  
		Last Modified: Tue, 19 Jul 2022 19:14:52 GMT  
		Size: 7.3 MB (7310337 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3bc5d40d77c389c1092f5c35566145ae29c7452a407d11562b411eb5448ad7c`  
		Last Modified: Tue, 19 Jul 2022 19:14:51 GMT  
		Size: 604.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5288b153492e8aa553122955d5030afe899e17d73edcd1c3c9cf99f3be0d097`  
		Last Modified: Tue, 19 Jul 2022 19:14:51 GMT  
		Size: 895.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:342c57f2ed9b552f85fbd309aa0d5cc201c5a163c44819d65726697f18f1275e`  
		Last Modified: Tue, 19 Jul 2022 19:14:51 GMT  
		Size: 668.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87f751ae619d28e8d6f5e3063e6698e5b97858bd3d0306eebe5a2a64ddba6544`  
		Last Modified: Tue, 19 Jul 2022 19:14:51 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
