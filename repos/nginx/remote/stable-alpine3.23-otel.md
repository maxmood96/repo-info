## `nginx:stable-alpine3.23-otel`

```console
$ docker pull nginx@sha256:46d5b1eeb9c3d5bba8343c748927be85122633a8c7556ec81ea174044c432f9d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:stable-alpine3.23-otel` - linux; amd64

```console
$ docker pull nginx@sha256:8288701b43f8bf19cceeebdaeaf38f5b267f6b258eacee73dda3c3ae80894125
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42768715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1a477584dc3d4516ae09d6bb43cc9b30d8d7400777dcd0e7abc8b0e51cd72e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:15:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:15:20 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:15:20 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:15:20 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:15:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:15:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:20 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:15:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:15:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:15:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:15:20 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:17:45 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:17:45 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:17:45 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:17:45 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 19 May 2026 21:32:19 GMT
ENV OTEL_VERSION=0.1.2
# Tue, 19 May 2026 21:32:19 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2761f2b929073faf02088d1cd321e4cdd3134ccb2eb483426a89aa7a29d17031`  
		Last Modified: Tue, 19 May 2026 20:15:25 GMT  
		Size: 1.9 MB (1870866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9819a9bca5c765aec514db7e90c3dee6d699c76a611b592d388629f4b0f665eb`  
		Last Modified: Tue, 19 May 2026 20:15:25 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9097b7c36bd7225e6e955ae7f0a02738f22dec88330b0816aa0c026386c1db79`  
		Last Modified: Tue, 19 May 2026 20:15:25 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5e180c5634daea39efda1a8d35ea781126257c98fa38cd0374f6edcaa86a6e2`  
		Last Modified: Tue, 19 May 2026 20:15:25 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61194bdf8809d67a4145f10fb09173c8e7a28b51da484e25eece0ba02643fa88`  
		Last Modified: Tue, 19 May 2026 20:15:27 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b213b30736dba71e4c92b43e31901658ff70cb96e46524740dce204b477c616`  
		Last Modified: Tue, 19 May 2026 20:15:27 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f27930cd22b2187112be5098b67ad2f8d4cb973c469535b47ce4f7724605ae03`  
		Last Modified: Tue, 19 May 2026 21:17:52 GMT  
		Size: 20.3 MB (20280246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0798c98bd941ce7bf30f19578736ee48b9ac2c2c94554b2f5c8b92a2209741d5`  
		Last Modified: Tue, 19 May 2026 21:32:29 GMT  
		Size: 16.7 MB (16748823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:bf60bbee0e90b54435e24825fdd702bd685f2d5b7ad5d9832eea1c6822295b7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1091520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7115d93dbb497eec53ee4a3503f071bcad1a9113036fbc464f2685dbcb2f838e`

```dockerfile
```

-	Layers:
	-	`sha256:e7655d41c7f2ab93fac6a3ea2946137433915417042be088617b3611911317e0`  
		Last Modified: Tue, 19 May 2026 21:32:27 GMT  
		Size: 1.1 MB (1071153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9cd87e2fbd7e07047075df48ff46908595c1fd3c5d23c81f2b3060c546a5050`  
		Last Modified: Tue, 19 May 2026 21:32:27 GMT  
		Size: 20.4 KB (20367 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:f207f096bea17c5d233ec86302493b9b989bca635e8ffdcd9ea8babf6c48d115
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41546157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dfb4b26fd727167c9e3077b7af18291099f1505d17b9bdbcfe21ea5bedd19a8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Fri, 22 May 2026 18:24:44 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:24:44 GMT
ENV NGINX_VERSION=1.30.2
# Fri, 22 May 2026 18:24:44 GMT
ENV PKG_RELEASE=1
# Fri, 22 May 2026 18:24:44 GMT
ENV DYNPKG_RELEASE=1
# Fri, 22 May 2026 18:24:44 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:24:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:24:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:24:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:24:44 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 22 May 2026 18:26:21 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:26:21 GMT
ENV NJS_RELEASE=1
# Fri, 22 May 2026 18:26:21 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:26:21 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Fri, 22 May 2026 18:30:44 GMT
ENV OTEL_VERSION=0.1.2
# Fri, 22 May 2026 18:30:44 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}         nginx-module-otel=${NGINX_VERSION}.${OTEL_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 cmake                 bash                 alpine-sdk                 findutils                 curl                 xz                 protobuf-dev                 grpc-dev             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && PKGOSSCHECKSUM=\"9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *60789259bfab36b1669a414881a9d002fd246d6b.tar.gz\"                 && if [ \"\$(openssl sha512 -r 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 60789259bfab36b1669a414881a9d002fd246d6b.tar.gz                 && cd pkg-oss-60789259bfab36b1669a414881a9d002fd246d6b                 && cd alpine                 && make module-otel                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85eeda869ba1f71ec25843c77bedd1ed161f244e20f9e34649c89eef6a7cfb26`  
		Last Modified: Fri, 22 May 2026 18:24:49 GMT  
		Size: 1.9 MB (1891358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efbbdc4b9230ad0e344fdfaf6c610be06abd8f8b5c299e027a51f4da6751cb1b`  
		Last Modified: Fri, 22 May 2026 18:24:49 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a77ff2fd3eb3c1ba3bbe79d903dccefbc4878310a44bf1c3462c79ed1b79bd9c`  
		Last Modified: Fri, 22 May 2026 18:24:49 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a02f4da3cdb6eb3330aa6e4be1cc7c8853c5008b03315a7413d4239d19cfa6eb`  
		Last Modified: Fri, 22 May 2026 18:24:49 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba6e64485597605500cbbf14827bc56c589b134fe9ac1ed10d54028ebba9c3f4`  
		Last Modified: Fri, 22 May 2026 18:24:50 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea3fdae34707bf56f738169361c460571f7bca3bebcc2fb92ac28180608e0c6`  
		Last Modified: Fri, 22 May 2026 18:24:50 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4a6cd5ad95a25f0842fa56b5563e658ac9331343a1d691551fe148bad584fd`  
		Last Modified: Fri, 22 May 2026 18:26:29 GMT  
		Size: 19.7 MB (19727420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1007fd2dc5af72981e4d4ff71abcb312e00af5ead3b32091657968934025a563`  
		Last Modified: Fri, 22 May 2026 18:30:51 GMT  
		Size: 15.7 MB (15722924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:7ca69cac41a86a56bd6c2173b7ffd538892d18015245ea9ee5cf30fb1fbabc7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.1 MB (1091078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f91ff4d3c8193741cfc69311bdeeb9481606778ea853ad6b24f9a5e5176d2bed`

```dockerfile
```

-	Layers:
	-	`sha256:b0d3b8618aad81202adde513b19ff163a4d006a73bba05cd523529dbc4e33f0f`  
		Last Modified: Fri, 22 May 2026 18:30:51 GMT  
		Size: 1.1 MB (1070583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adeea5f642b3d99bad67bbc3ccb077d12b358a9e52a8df4319cdd288a1e45d53`  
		Last Modified: Fri, 22 May 2026 18:30:51 GMT  
		Size: 20.5 KB (20495 bytes)  
		MIME: application/vnd.in-toto+json
