## `nginx:stable-alpine3.23-perl`

```console
$ docker pull nginx@sha256:4b98ea12a4298a587d91f46759f8d2695ac6e4e8442b857a6ca36963c0dd7df3
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

### `nginx:stable-alpine3.23-perl` - linux; amd64

```console
$ docker pull nginx@sha256:29106a88d2dcead1520985c0ead084e96e05d572fe32cc6a7d5698cc6a5dd4ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.3 MB (36313338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:844ce7ecbf38e3103b36f62c956683f89280f1160354350099179cdc634ca76a`
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
# Tue, 19 May 2026 21:31:22 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed -E 's,nginx-module-acme=[^ ]+,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
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
	-	`sha256:d500975e8e4fcdb4a9b91c8e35eef652bb22831f6aa7ed6b9e902b580f28ffba`  
		Last Modified: Tue, 19 May 2026 21:31:29 GMT  
		Size: 10.3 MB (10293446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:ab2e3d4df1b72018e6ae04267f067dacde8d647c2cfdf2cb20d3eb6e88def8b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1870293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:797f9269ef15cbe20a4fbe7c520134b4446ac905279866650678763f8757845a`

```dockerfile
```

-	Layers:
	-	`sha256:5e0ae5ddf6b181e69a24d08d33fad8020c37ae348f1c154b9fbe4e86e4f2a0f8`  
		Last Modified: Tue, 19 May 2026 21:31:29 GMT  
		Size: 1.8 MB (1849942 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:159f39e3e7a88820cdf341b3d2c205b2d10892dfc10a752e42e354486c54e34b`  
		Last Modified: Tue, 19 May 2026 21:31:28 GMT  
		Size: 20.4 KB (20351 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-perl` - linux; arm variant v6

```console
$ docker pull nginx@sha256:40fc4a0a8ba83d579864bd791bdc003ba61bbb4010dc695267568674be1b7553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.1 MB (29102837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d36a464a39e7dd71b28bf4f9d22879f0f338399e37e8093d3ee39cc434b7d938`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:14:50 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:14:50 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:14:50 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:14:50 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:14:50 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:14:50 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:50 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:50 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:14:50 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:14:50 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:14:50 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:19:02 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:19:02 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:19:02 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:19:02 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 19 May 2026 21:30:59 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed -E 's,nginx-module-acme=[^ ]+,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a31c00b8a662898b9dcf87053135b72f1e9bb1f46cf700421b2ed8bd76d871`  
		Last Modified: Tue, 19 May 2026 20:14:54 GMT  
		Size: 1.9 MB (1868359 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05e241c6e39aebdf1ac730f0c65818e66e19016d6c6b077c819699fff4204f82`  
		Last Modified: Tue, 19 May 2026 20:14:54 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f583d3d971038ab4022c2ad2b3618ed045458a82f4b2c335b44370d6016c6696`  
		Last Modified: Tue, 19 May 2026 20:14:54 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c582e44a1b61b1d14ccf2fd54fe70ae5552e65417ac33be95f65ff2035772f42`  
		Last Modified: Tue, 19 May 2026 20:14:54 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34aa47f7eba443d27b3060ed5f4dea30ac1cfb5e12034bb06127cf60114f8043`  
		Last Modified: Tue, 19 May 2026 20:14:55 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98fe0da14221b4e03caf3c459b42d752b4326298bc2694cb2722786586d79c7d`  
		Last Modified: Tue, 19 May 2026 20:14:55 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:426aafaffc6df67ff96347f9d660ebec48769f96c63b2a2041d06436b0624bae`  
		Last Modified: Tue, 19 May 2026 21:19:08 GMT  
		Size: 14.1 MB (14141089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77b53aa18edf642e3bd7b826028cb0f5660d3f80fc3f2ef1bd53c7a3055e5952`  
		Last Modified: Tue, 19 May 2026 21:31:05 GMT  
		Size: 9.5 MB (9516932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:a7f11bc6c16d4487803c38b772e9b3e597a223cdac294f7bc5c82f0db79a2bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 KB (20231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60683537978e446db9abc3871d9f0483fb516718c449e228d508564debcdc004`

```dockerfile
```

-	Layers:
	-	`sha256:13643c5f3ac0e97fbe8f9bc7f7d6b10232bcc1a0b36a7786de79b68c0f2f53a2`  
		Last Modified: Tue, 19 May 2026 21:31:04 GMT  
		Size: 20.2 KB (20231 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:4d5d23e160cf30a1b390f9c9c95d128c1752f8e7cf90e4942b670aa685684aa4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **31.0 MB (30987707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55b2ffaeb385c0b5aa36077cd81495d055809920ae053f47200e4dd4ce1de652`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:16:07 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:16:07 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:16:07 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:16:07 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:16:07 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:16:07 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:07 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:07 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:07 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:16:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:16:07 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:16:07 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:16:07 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:24:03 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:24:03 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:24:03 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:24:03 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 19 May 2026 21:31:32 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed -E 's,nginx-module-acme=[^ ]+,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8761a1571c43cdb397af90534a587c7e2a0027efdad5c82315e2b6e140d37f7`  
		Last Modified: Tue, 19 May 2026 20:16:13 GMT  
		Size: 1.7 MB (1693744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:257703971266e076ab77fb61ff807e2811f036aba4ce968e4e15a5f9c8fe6f0e`  
		Last Modified: Tue, 19 May 2026 20:16:13 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c11719d836683ba0677a22ddecef9b3fa565ffac736ec15a72803558b160959d`  
		Last Modified: Tue, 19 May 2026 20:16:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcab1a3a73262c570591cb23f718bdc59b0bfd2ce4fc89737b27133605c46eb1`  
		Last Modified: Tue, 19 May 2026 20:16:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be6b1cd53643618eca445ff4e2b3455fcc8dfb1d7d5710547cd103ecf6668532`  
		Last Modified: Tue, 19 May 2026 20:16:14 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f336042598605c97ea13ceb5b28f5d83cc0c108582ba5c274b4286cbc0a0bd9f`  
		Last Modified: Tue, 19 May 2026 20:16:14 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b15ff233652cc2e1573e656e6dc34138abf4d4e85e1c17318e558adb8fa6b9c`  
		Last Modified: Tue, 19 May 2026 21:24:11 GMT  
		Size: 16.7 MB (16654460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f28bfdfbcb2a75f4194b1840c5cea036a3bdf734d45e8f1d42cd7822d7fbfce8`  
		Last Modified: Tue, 19 May 2026 21:31:39 GMT  
		Size: 9.4 MB (9351782 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:a6b6bbc9f878f18890e07fc28e8a58e145d4b8102341959d515116419e052af1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1869802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c883e6b67699ab7f8b79201b344ab8350f1634b6fe115120041c267dba2a636`

```dockerfile
```

-	Layers:
	-	`sha256:9d5b2b7ef56d98c5d3667e012fa1e98ead6f0231984927c1db9f2d837933cd58`  
		Last Modified: Tue, 19 May 2026 21:31:39 GMT  
		Size: 1.8 MB (1849356 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a466bc65f85d89295e4d1ffe1440787b817747b7bde913b2b4d900368b162804`  
		Last Modified: Tue, 19 May 2026 21:31:39 GMT  
		Size: 20.4 KB (20446 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:142bd3b755a46b8365e19f9e139ff3fc9971b0d650f7499981a8ed5d1e2530f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36060759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1f4488529e122d5ca2b99d24dd28511f5c27c797ddee96462ebef7d86c7a4b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:14:22 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:14:22 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:14:22 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:14:22 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:14:22 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:14:22 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:22 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:22 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:22 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:14:22 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:14:22 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:14:22 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:17:34 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:17:34 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:17:34 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:17:34 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 19 May 2026 21:31:40 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed -E 's,nginx-module-acme=[^ ]+,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfa022fb2950cf6a4cbda5d710f2e9bc1d9316a151f841e9f20e57373c989d56`  
		Last Modified: Tue, 19 May 2026 20:14:33 GMT  
		Size: 1.9 MB (1891337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96bdd898123491de0059fe33c64f4d771ece1780188374b7089604eed1f7dda4`  
		Last Modified: Tue, 19 May 2026 20:14:32 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d11e82a130775c75781b308fba758ce0cbb51ab8b3728b822d9ba81e1aaa4fa`  
		Last Modified: Tue, 19 May 2026 20:14:32 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:371cab2d29d6d0c4517510ea0adb78510a20ed212ac215c85afe4eb8357a5081`  
		Last Modified: Tue, 19 May 2026 20:14:33 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad3ecb13825b9bb398bce18a425d9af6bcae0e9999cf565600dd80d9413ff4e2`  
		Last Modified: Tue, 19 May 2026 20:14:34 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f374a8b24334edc45e1d527473b4004a096c488c3c76bce267f475e4eb73c15c`  
		Last Modified: Tue, 19 May 2026 20:14:34 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d37e74ecc4aaadc3a8ba682c3f558159d3ff43814b161ee7ecce13b62ba2d5c`  
		Last Modified: Tue, 19 May 2026 21:17:41 GMT  
		Size: 19.7 MB (19727313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209ea52336dee441f16e2ed5ca638da85f6a13871f4b77883dccec35777fb14a`  
		Last Modified: Tue, 19 May 2026 21:31:48 GMT  
		Size: 10.2 MB (10237652 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:23473c14947482d07a98d784d95c377f0180e5ef8a147df9f20d2da1028c203c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1869853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a94f5c179bf22d60466fd77e6d54fce55ae897a6db8e6b73ebd060c6e6e35a40`

```dockerfile
```

-	Layers:
	-	`sha256:a0962b39232de19f7e57a1911733f08b380ccdbee735295cb27b74c516818dd2`  
		Last Modified: Tue, 19 May 2026 21:31:47 GMT  
		Size: 1.8 MB (1849374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28466581176a51af760b0a0d28dd99f374910ec709bcedc9351914929dac1baf`  
		Last Modified: Tue, 19 May 2026 21:31:47 GMT  
		Size: 20.5 KB (20479 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-perl` - linux; 386

```console
$ docker pull nginx@sha256:3165e856fec28dd26c29e188fc49a426b442f61d0005b8db6ece14f09bbdf030
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **35.1 MB (35130505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30a7bb288f75af83ec682cfe47115cba2407718b998763b9a203eb31d64f6694`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:17:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:17:09 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:17:09 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:17:09 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:17:09 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:17:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:17:09 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:17:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:17:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:17:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:17:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:17:09 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:17:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:17:09 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:21:49 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:21:49 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:21:49 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:21:49 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 19 May 2026 21:29:45 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed -E 's,nginx-module-acme=[^ ]+,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54139fa8090c86122e7504ab7f3fa1f075873077750a66bd014ad502e7c1945`  
		Last Modified: Tue, 19 May 2026 20:17:14 GMT  
		Size: 1.9 MB (1944722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb0bdc3d26779c5af19cae796d413c6c375cc4d78f9d3cfb582a4e644fee2918`  
		Last Modified: Tue, 19 May 2026 20:17:14 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00ea2dfa0ea689f9d27579cfe3eb7ac62ae572eee50b56e7b71a08b0a8480d27`  
		Last Modified: Tue, 19 May 2026 20:17:14 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6ea616cfc57f66e98e8fe3ff973913a8f3c1586b325270a930e4214674b90b5`  
		Last Modified: Tue, 19 May 2026 20:17:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2cd170edc62d520ad1b67997e9f3c65237e93cdd790265d33c55731fe8444a5`  
		Last Modified: Tue, 19 May 2026 20:17:16 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ddbe2c65467f5c8badc0c57240801fbc93278ab37213f26c3faf08c2fe8a5d`  
		Last Modified: Tue, 19 May 2026 20:17:15 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00da04c52b0927658980b427ef95e413c43a1f82400d83d07ea4095fc79f8f30`  
		Last Modified: Tue, 19 May 2026 21:21:57 GMT  
		Size: 19.7 MB (19662614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb4736d054a1783670cafb7d03cf9c9631c46553ced458ce20e9ebec02af68f`  
		Last Modified: Tue, 19 May 2026 21:29:53 GMT  
		Size: 9.8 MB (9828131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:95df1b1c11aeef0ad907f3cc6dde133f53a357e11893ea15a0eeded3b7881c55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1870223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba46d47d90b4c073b8af2c4ac70f48fb611edf385be32796562b3249b95de17a`

```dockerfile
```

-	Layers:
	-	`sha256:65097383fee82b5a1c91c04c435ebd6c8d872218c36241c43e67153abd8ba030`  
		Last Modified: Tue, 19 May 2026 21:29:52 GMT  
		Size: 1.8 MB (1849915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32063e4c988a487d7a1dd771471410a6370c7aefed0f030d6598883bea753adf`  
		Last Modified: Tue, 19 May 2026 21:29:52 GMT  
		Size: 20.3 KB (20308 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:344fe588ea3063dfe21aff34505e66f939ab8bb1639af0502681ad13a9f05400
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36825724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d421c8b51a3c76b0f76f5b2b6ddf664e036b9c14bbfdeca8d02612ed07e7cf43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:30:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:30:20 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:30:20 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:30:20 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:30:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:30:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:30:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:30:21 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:30:21 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:30:21 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:26:03 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:26:03 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:26:03 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:26:03 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 19 May 2026 21:30:11 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed -E 's,nginx-module-acme=[^ ]+,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43dd9024439080c5fee6414b5c4ed3fb67a4cba6098ea0797ba5845404b7a1d3`  
		Last Modified: Tue, 19 May 2026 20:30:30 GMT  
		Size: 2.0 MB (1963367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63905ea5b150d55f3b79b38a5490837c24037c7abd8acd1d4162ee05f5a4e83a`  
		Last Modified: Tue, 19 May 2026 20:30:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e343a2d6005f8b44b118ecd9d16bb3fb9be2c89363fec6739559a23202a55e`  
		Last Modified: Tue, 19 May 2026 20:30:30 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3de67dcc89abc325cda51ea490a783c6d19781f93c56373d1a93cf5382c124f`  
		Last Modified: Tue, 19 May 2026 20:30:30 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:686191425faec729397c7fbe27f40b57c8d3eb25035da6b50c85bab3f035a90c`  
		Last Modified: Tue, 19 May 2026 20:30:31 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8938cd886756583b3e2e8f621d2518666da25bb8a79ddb2882b181f90749810f`  
		Last Modified: Tue, 19 May 2026 20:30:31 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1071e2b8e443aeb6dd786e344c945cf2caa6830b85ee98d5c665836738318644`  
		Last Modified: Tue, 19 May 2026 21:26:16 GMT  
		Size: 20.5 MB (20520283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19dc30d75e7b42f4f03752ded6393329d232de7e63a95b1f67c5f63d11a14eaf`  
		Last Modified: Tue, 19 May 2026 21:30:28 GMT  
		Size: 10.5 MB (10506553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:8a248fa9c97e74c2f4ce1ac908b7015cdceea3c536e085ec57ed0a7d2e69a8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1869746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0125e442fd123b8efd28deac68f4586ecf538e457211a4a8f01ced9c8147eac4`

```dockerfile
```

-	Layers:
	-	`sha256:c7bbb81e2080e925c5f4b1f6562d9709c62057f416313e1487c2cfd04ec84fef`  
		Last Modified: Tue, 19 May 2026 21:30:28 GMT  
		Size: 1.8 MB (1849339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cc08f7ce0e529a7b98427e0fcb064f14a5a5aedebebc7ee08d82c1f49b9c039`  
		Last Modified: Tue, 19 May 2026 21:30:27 GMT  
		Size: 20.4 KB (20407 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-perl` - linux; riscv64

```console
$ docker pull nginx@sha256:8343d5181d2540e341672063ae0fa8b8d61d857f77b02a5ecdfd72568bcd41c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.3 MB (33293533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67d415dd5bb60e3fd47a7942f43fd58874e68fef7b16d77736b496c68c186dab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 14 May 2026 09:55:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 14 May 2026 09:55:09 GMT
ENV NGINX_VERSION=1.30.1
# Thu, 14 May 2026 09:55:09 GMT
ENV PKG_RELEASE=1
# Thu, 14 May 2026 09:55:09 GMT
ENV DYNPKG_RELEASE=1
# Thu, 14 May 2026 09:55:09 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:55:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 May 2026 09:55:09 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:55:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:55:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:55:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:55:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 May 2026 09:55:09 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 09:55:09 GMT
STOPSIGNAL SIGQUIT
# Thu, 14 May 2026 09:55:09 GMT
CMD ["nginx" "-g" "daemon off;"]
# Fri, 15 May 2026 22:18:20 GMT
ENV NJS_VERSION=0.9.8
# Fri, 15 May 2026 22:18:20 GMT
ENV NJS_RELEASE=1
# Fri, 15 May 2026 22:18:20 GMT
ENV ACME_VERSION=0.4.1
# Fri, 15 May 2026 22:18:20 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Sat, 16 May 2026 19:14:23 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed -E 's,nginx-module-acme=[^ ]+,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:689107f9f1d59e7bb0f938d60457bc810afe4b50eddb5f857b434989192f4286`  
		Last Modified: Thu, 14 May 2026 09:55:34 GMT  
		Size: 1.9 MB (1917651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dde034249836e61741a92b5e48e68ab9ef961434115e9e77e6f1766c4352b3`  
		Last Modified: Thu, 14 May 2026 09:55:34 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88cf74e84abb570036adc571f867035701610acbd81bea32715c2342ec46ac74`  
		Last Modified: Thu, 14 May 2026 09:55:34 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9fd7a037fd23bb8a49bbc10439a3b54903b32b701f4b05b79432827450f6b8a4`  
		Last Modified: Thu, 14 May 2026 09:55:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86b4b5cedec3bf71566c53a2171eee6b2e06acbc38d94747d7afcf18ad3e4f06`  
		Last Modified: Thu, 14 May 2026 09:55:35 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7ac331673b50ac8fae1eb29bc0352649f90a2c648d89d7f39245ae3c452a4d5`  
		Last Modified: Thu, 14 May 2026 09:55:35 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c37c00480454fd124b96f34830ae7fac86850c52557669160b32fe80583728f4`  
		Last Modified: Fri, 15 May 2026 22:19:10 GMT  
		Size: 18.1 MB (18052132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff94e11675689f998a2b732a21fecbee9ab2cba1e7b42cf9fc0f29eb0b9f2066`  
		Last Modified: Sat, 16 May 2026 19:15:23 GMT  
		Size: 9.7 MB (9731498 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:bf816908626c04a04488c9b06cddc58a64d6f7ad8f8cf9a1bce745e0670a59fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1871230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f888fc4bea1ef20a67e37efc495ed867e2f6605f7f4448fe5c9fd8fd2558ba3`

```dockerfile
```

-	Layers:
	-	`sha256:4a50ce92b62210f04960272f6dcebc28f2ae209c5f9e7c8abaf2064524eec8cb`  
		Last Modified: Sat, 16 May 2026 19:15:21 GMT  
		Size: 1.9 MB (1850929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9994a02e6545520d7fb8157490c8e03e96a78ada879fb7cdf470906567df03c7`  
		Last Modified: Sat, 16 May 2026 19:15:21 GMT  
		Size: 20.3 KB (20301 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine3.23-perl` - linux; s390x

```console
$ docker pull nginx@sha256:115ac41440b57e33d5944d8e060b081f513c388a669bc10912e2bf25a055fbe3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.9 MB (36934593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84b46a1ef3a951f33c8425f79f27a8b9477c2097baff92a919fb924c24fa77eb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Tue, 19 May 2026 20:14:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:14:16 GMT
ENV NGINX_VERSION=1.30.1
# Tue, 19 May 2026 20:14:16 GMT
ENV PKG_RELEASE=1
# Tue, 19 May 2026 20:14:16 GMT
ENV DYNPKG_RELEASE=1
# Tue, 19 May 2026 20:14:16 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make base                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && DEPS=$(apk query --summarize depends --recursive --no-cache                        --repository "@nginxorg ${tempDir}/packages/alpine/"                        ${nginxPackages/=/@nginxorg=})             && apk add --no-cache $DEPS             && apk add --repositories-file /dev/null -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache gettext-envsubst     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:14:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:14:17 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:14:17 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:14:17 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 19 May 2026 21:20:31 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 21:20:31 GMT
ENV NJS_RELEASE=1
# Tue, 19 May 2026 21:20:31 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 21:20:31 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils                 curl                 cargo                 clang-libclang             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && export BUILDTARGET=\"module-geoip module-image-filter module-njs module-xslt module-acme\"                 && if [ \"\$(apk --print-arch)\" = \"armhf\" ]; then BUILDTARGET=\"\$( echo \$BUILDTARGET | sed 's,module-acme,,' )\"; fi                 && make \$BUILDTARGET                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed 's,nginx-module-acme=.*,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
# Tue, 19 May 2026 21:30:06 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-r${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}.${ACME_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 perl-dev                 bash                 alpine-sdk                 findutils                 curl             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && PKGOSSCHECKSUM=\"83a117b77bf3f1ce7f227b75712766c1dec6bcfae0f1f87a9d522d1ef9b66a8ca550c3c0835b82e74e1242284be65126a1858a4fabd1dc9969ce8a7fd8e4681b *3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz\"                 && if [ \"\$(openssl sha512 -r 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 3fdb8a9a864e5680a1d432aab681e40b7e269bb4.tar.gz                 && cd pkg-oss-3fdb8a9a864e5680a1d432aab681e40b7e269bb4                 && cd alpine                 && make module-perl                 && apk index --allow-untrusted -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && if [ "$apkArch" = "armhf" ]; then nginxPackages="$( echo $nginxPackages | sed -E 's,nginx-module-acme=[^ ]+,,')"; fi             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi # buildkit
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b718a481eb6a1e5f2702e58138ca2c5777099b6cc9261b3ee04793b43d6020f`  
		Last Modified: Tue, 19 May 2026 20:14:28 GMT  
		Size: 2.0 MB (1989873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4018e9f1117d94f9914bcae655876ec203350c75c066f70bdad78edad676d4a8`  
		Last Modified: Tue, 19 May 2026 20:14:28 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e419add5f5b4e45c14b8e385639597a6e0349f06fb065a0464bdfe68f0b80b4`  
		Last Modified: Tue, 19 May 2026 20:14:28 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a49ff5d09575651be88dbf61d1dc5b6fb3938ba26cdda3be8c819813395fa87f`  
		Last Modified: Tue, 19 May 2026 20:14:27 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e839d4891e79770219b732c3961d69c0a218ba39a8da712870b91b933dafa7c`  
		Last Modified: Tue, 19 May 2026 20:14:29 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c343d5fa069debb586f160051765d31650ec33eaf57f468c92e62a60a6350803`  
		Last Modified: Tue, 19 May 2026 20:14:29 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c52566b1e9fdb4348ac60c7634f9a1ecda25b3b227a8e64350219c2646a8739b`  
		Last Modified: Tue, 19 May 2026 21:20:43 GMT  
		Size: 20.4 MB (20373634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3edbf199d3c6dd9f4e96a99079f2ac74882a87a27b43e08f3f567b29bada809`  
		Last Modified: Tue, 19 May 2026 21:30:20 GMT  
		Size: 10.8 MB (10839961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine3.23-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:3e08e6f217c48f12ef734a339a788b57195b45fe8e9a535d588ae2db6ea217ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 MB (1869640 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e47dd18b3f371f31bf2569f4cacd1c6c3e86a3ccee26105ab8356fe41fa928f`

```dockerfile
```

-	Layers:
	-	`sha256:af909b2c7557f91e46ffeb1c203808e3f9adeb2b052b0f582a7c8422cc8e7790`  
		Last Modified: Tue, 19 May 2026 21:30:19 GMT  
		Size: 1.8 MB (1849289 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:87aeece16d5bfb0703f205ff1e407d731f0a858a614d313e9c0863424e91bc3d`  
		Last Modified: Tue, 19 May 2026 21:30:19 GMT  
		Size: 20.4 KB (20351 bytes)  
		MIME: application/vnd.in-toto+json
