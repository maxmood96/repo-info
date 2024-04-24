## `nginx:mainline-alpine`

```console
$ docker pull nginx@sha256:531d6ee69f5363d1e90bb40feb944ee47c806a68f439c7687f7653c359cf83f1
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

### `nginx:mainline-alpine` - linux; amd64

```console
$ docker pull nginx@sha256:542a383900f6fdcc90e1b7341f6889145d43f839f35f608b4de7821a77ca54d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.4 MB (20437674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11d76b979f02dc27a70e18a7d6de3451ce604f88dba049d4aa2b95225bb4c9ba`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 17:12:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 16 Apr 2024 17:12:08 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 16 Apr 2024 17:12:08 GMT
ENV PKG_RELEASE=1
# Tue, 16 Apr 2024 17:12:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"74000f32ab250be492a8ae4d408cd63a4c422f4f0af84689973a2844fceeb8a3e7e12b04d7c6dac0f993d7102d920a5f60e6f49be23ce4093f48a8eb1ae36ce5 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 17:12:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Apr 2024 17:12:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Apr 2024 17:12:08 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 16 Apr 2024 17:12:08 GMT
ENV NJS_VERSION=0.8.4
# Tue, 16 Apr 2024 17:12:08 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"74000f32ab250be492a8ae4d408cd63a4c422f4f0af84689973a2844fceeb8a3e7e12b04d7c6dac0f993d7102d920a5f60e6f49be23ce4093f48a8eb1ae36ce5 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49890e937b90b500d8928c7c8d8e5e240077d58d0af49c0ac37b63dedd75d326`  
		Last Modified: Wed, 17 Apr 2024 16:53:06 GMT  
		Size: 4.0 MB (3984272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4d1f9351edbe6d5ae798d5a904ebb5ff9c77302151bfffd7e89ce43822babbf`  
		Last Modified: Wed, 17 Apr 2024 16:53:05 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20251c300f57ddc900fcf54b340621c6ccab71b757a15e50657480ad55d87326`  
		Last Modified: Wed, 17 Apr 2024 16:53:05 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0bc9bec79d15ff29478aacc798f358df8732e680cdc9d8f7abdc5738f017bcb`  
		Last Modified: Wed, 17 Apr 2024 16:53:05 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e9a094d2fe0c6ba7ed65ebae54ed3ee1998f2a2dcc9f6c93320648f4a9f9eca`  
		Last Modified: Wed, 17 Apr 2024 16:53:06 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2fb8c57dcab0009021dc21ed7b9373adad4b225c3b89da601732386c57ee0e`  
		Last Modified: Wed, 17 Apr 2024 16:53:06 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e979eecfde6209c789555a2d14d05e677829f57558a788399a75581ffcde3ed6`  
		Last Modified: Wed, 17 Apr 2024 17:49:18 GMT  
		Size: 13.0 MB (13040094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:18098ec1b423d08547f2e878576cf578c9bb39c748c2f128d4cf76d70184a996
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1255220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092bd01a6a1212a566e761cddf603d68e170b720aca3b916db3fd5a9f8c5f01b`

```dockerfile
```

-	Layers:
	-	`sha256:e3243f6249724a4a18d1d54f7aecef453701d41d664c09453f7fc72852f60d4b`  
		Last Modified: Wed, 17 Apr 2024 17:49:17 GMT  
		Size: 1.2 MB (1231157 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1bb3f7c1635b24d8c44c88b6ef373f8e3abc16849e115993846bbd6bafaef763`  
		Last Modified: Wed, 17 Apr 2024 17:49:17 GMT  
		Size: 24.1 KB (24063 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine` - linux; arm variant v6

```console
$ docker pull nginx@sha256:d308cda0b219089f9c1c9c33d4dfd0b67dad20ee95e331dd0b343c906e368bbf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.0 MB (17956019 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6bed1b64316aec99e7a866ef8a9bc08f6a08866226fb3bc1c0804039367545`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 21:35:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 21:35:33 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_RELEASE=2
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5d7ad3edc2c31f1b91f341f1b43a7ccb5604e115473e1eb44a59a53ed935ac3`  
		Last Modified: Wed, 24 Apr 2024 01:03:00 GMT  
		Size: 3.8 MB (3801192 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1db4c7bec291d8d12ef19e74feec61ca115de6e56a4cc90c2cac8f614e0c18`  
		Last Modified: Wed, 24 Apr 2024 01:03:00 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc9e766483a5563587d78092bab885de04aba2fa3300960a69793c8f1c809c61`  
		Last Modified: Wed, 24 Apr 2024 01:02:59 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f40f969ae84188e6e4ac02c751805b33d1756d21cfe3ce493f5d6c11df3c756c`  
		Last Modified: Wed, 24 Apr 2024 01:02:59 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc3c788161432949716bda7cd1b238ed46c498278073a1bd0b77089d7a50c5c9`  
		Last Modified: Wed, 24 Apr 2024 01:03:00 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14bc8739a7604f2b73478d3634537d7f5c9a96190cc67f2d760fc866a0daa4e2`  
		Last Modified: Wed, 24 Apr 2024 01:03:00 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e080dbbba82dd06bbfffca6133f9205c4a2fc0b53bfba40c8f9390cf4d6c39fe`  
		Last Modified: Wed, 24 Apr 2024 01:56:39 GMT  
		Size: 11.0 MB (10984853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:e6a1a4bfc4200bfb88575d53d20952692df698c14bc5bc3b235321a2067d7e6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 KB (21671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6018312b2c009672a9ef4d685f39b7a2d5c9ef4a292046924d7f394431301d2e`

```dockerfile
```

-	Layers:
	-	`sha256:1ee07a78fcc46b3805553bc28e8c8a41e9034461f42db89c557cad9fd994744d`  
		Last Modified: Wed, 24 Apr 2024 01:56:37 GMT  
		Size: 21.7 KB (21671 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine` - linux; arm variant v7

```console
$ docker pull nginx@sha256:3403e4f410a9b94907624a2423bea74dbbf972084eb11f9f93d8e1fc78d7935c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.4 MB (17368079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:00bd5c5989455cc2998beb3bfdefcf3b147b9398c491c902ed6f3bdb6ab536ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 21:35:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 21:35:33 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_RELEASE=2
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6026656fca4ff7a6128d9f41584be9bd768f09b0be919aa4e1b127fa55c83f8e`  
		Last Modified: Wed, 24 Apr 2024 01:24:35 GMT  
		Size: 3.5 MB (3512923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c78f111efc772c01a556e9abe1f1d194be1aba302083f318f42d7e353d8a3db0`  
		Last Modified: Wed, 24 Apr 2024 01:24:35 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3dd1b49bf7bedf5628e47e10908e00b8fefe8cc4727f3cb9496041f0b731b86`  
		Last Modified: Wed, 24 Apr 2024 01:24:35 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f080b3db0c2a0f59aa3ea5ee125c56db95487ee81481051ec460edb54ebfdcaa`  
		Last Modified: Wed, 24 Apr 2024 01:24:35 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05719c4a15205c0d04a8a6a4230817d9589f620e66a514e023f47d38a2920a56`  
		Last Modified: Wed, 24 Apr 2024 01:24:36 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1af9cc1eac6f4dbf81cef3a533e366683e10aa534f713ce95aaae26e60016f1`  
		Last Modified: Wed, 24 Apr 2024 01:24:36 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:487f2741b9703581e3d347cd3d29bed7064d654ddc4e549bb2868aba44dd4465`  
		Last Modified: Wed, 24 Apr 2024 02:09:06 GMT  
		Size: 10.9 MB (10931669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:b9120d6db3facaa086d043040a9b3b1cd5f1cde5de35e978a56855067d7632ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1255708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a04f2a5e82dc0d944a278165645869c9ee395a43023b74c986ed78deb30bf04e`

```dockerfile
```

-	Layers:
	-	`sha256:6699d5375cb5b91212a7e28bacda80db43cdcc336f02694452b5e29e9775cfd4`  
		Last Modified: Wed, 24 Apr 2024 02:09:04 GMT  
		Size: 1.2 MB (1233819 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edb20a542837c61e9d10eb99568aad152cfb17bad838bb02b483687328680d57`  
		Last Modified: Wed, 24 Apr 2024 02:09:04 GMT  
		Size: 21.9 KB (21889 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:a07ebd3327070119b352a40a59fc67c0a40ed9bca13508bfce06f9d8b9ec4000
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.2 MB (20170266 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f49f2e3796058c0b6568d610301043df2a2e84c72822ed0e2efdbcc4b653edc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 17:12:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 16 Apr 2024 17:12:08 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 16 Apr 2024 17:12:08 GMT
ENV PKG_RELEASE=1
# Tue, 16 Apr 2024 17:12:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"74000f32ab250be492a8ae4d408cd63a4c422f4f0af84689973a2844fceeb8a3e7e12b04d7c6dac0f993d7102d920a5f60e6f49be23ce4093f48a8eb1ae36ce5 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 17:12:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Apr 2024 17:12:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Apr 2024 17:12:08 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 16 Apr 2024 17:12:08 GMT
ENV NJS_VERSION=0.8.4
# Tue, 16 Apr 2024 17:12:08 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"74000f32ab250be492a8ae4d408cd63a4c422f4f0af84689973a2844fceeb8a3e7e12b04d7c6dac0f993d7102d920a5f60e6f49be23ce4093f48a8eb1ae36ce5 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fecb01b084106e7044ce580c32c8d732eadb5c3dedc768fd1c6f4b37e766fbc`  
		Last Modified: Wed, 17 Apr 2024 16:53:34 GMT  
		Size: 3.9 MB (3902601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dcdfb3bd786b97922a57a47ee3fa580bc8b6fb8f270b23d4971b39a42c3802e`  
		Last Modified: Wed, 17 Apr 2024 16:53:34 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3c5a0410e9dbea185dbea3a429552d3b497c54a4e70f3796b3a632233334870`  
		Last Modified: Wed, 17 Apr 2024 16:53:34 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29690876708ca474e46c75da07546ba5b7b771932be48915ac21cf4dd13f57fa`  
		Last Modified: Wed, 17 Apr 2024 16:53:34 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989b87cbc910a3b536dce261f967158d098601a4433e2269753a010bf63d33de`  
		Last Modified: Wed, 17 Apr 2024 16:53:35 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97e6ce245a93feed9a6c69346005f02992fad6490dc2bd88a06974f50eaaae7a`  
		Last Modified: Wed, 17 Apr 2024 16:53:35 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:602ab78e9e5b1133066113453303ac48887f36daabadceaacff74cc4b3f908db`  
		Last Modified: Wed, 17 Apr 2024 17:51:17 GMT  
		Size: 12.9 MB (12915367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:103f1404f5658944243a4992bd8761a42023dcd2e078d9c615d082b9ac21ec44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1255288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f26fb35c9f32afd6fa6a2141dfba38f914a291a0041740a081808063e5099362`

```dockerfile
```

-	Layers:
	-	`sha256:fb59bafebdc1b1b441ac9f583bf0323edf01ae7f08a956ea3266b5cf107ec7fd`  
		Last Modified: Wed, 17 Apr 2024 17:51:16 GMT  
		Size: 1.2 MB (1231180 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2cba093b13b083d9d85bf2c31982b6e78fd61f17f07122ad3721dccb8c5052d`  
		Last Modified: Wed, 17 Apr 2024 17:51:15 GMT  
		Size: 24.1 KB (24108 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine` - linux; 386

```console
$ docker pull nginx@sha256:dd9d95341ea1531654195b029711de3aace896be06ff5fc412becfcd9c36b6de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.3 MB (19255164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:244f8029d15cb6734d130d7d6b8585df04407eab2822fdfe0d726ac73f09d0c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 23 Apr 2024 21:35:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
EXPOSE map[80/tcp:{}]
# Tue, 23 Apr 2024 21:35:33 GMT
STOPSIGNAL SIGQUIT
# Tue, 23 Apr 2024 21:35:33 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_VERSION=0.8.4
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NJS_RELEASE=2
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${NJS_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/93ac6e194ad0.tar.gz                 && PKGOSSCHECKSUM=\"d56d10fbc6a1774e0a000b4322c5f847f8dfdcc3035b21cfd2a4a417ecce46939f39ff39ab865689b60cf6486c3da132aa5a88fa56edaad13d90715affe2daf0 *93ac6e194ad0.tar.gz\"                 && if [ \"\$(openssl sha512 -r 93ac6e194ad0.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 93ac6e194ad0.tar.gz                 && cd pkg-oss-93ac6e194ad0                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3e1f05bd8cb7333c74b215b1e4e51e0caa31ee875a8bc7fd7ec813f7782b394`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 4.0 MB (4013687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1e2de10a79a3a8d82361c78b4a0916b5433ee2656fe4be4147705fb593bb261`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78a28f949925323ea485ba5cd2cb717fee5fe7131500ddb59935b5139177999c`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c1f8d68231429ad020d78c1eff14e94c8a9e8b98d959e1f88c91a6ff2f3c541`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d763c348df487566d3bd36f5f6f6e297073cc2746eee2c928b823e86b2a869a`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2237cce1a4f8a3660aeb58d2ea9817a36bdcdb44a2176314bc981ae62a9cdb1`  
		Last Modified: Wed, 24 Apr 2024 00:52:21 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ea819715b1fbd4b757f3a82eca0bc2b1a9069aa1bcf6ecd870e75b7b6790a5a`  
		Last Modified: Wed, 24 Apr 2024 01:54:00 GMT  
		Size: 12.0 MB (11992807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:0f7de6b59d460d791b49adfb1dacc8b6141dbb4ea3df49b69aee69fe9d28347c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1252787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e4e4d0c5f756b5ff3d273844e5b8694ffbb52008451826f61c7a0b951702bc`

```dockerfile
```

-	Layers:
	-	`sha256:f76b8adec8818a73052a905a269e29742e3393290cbf95bb7855083d0f09bd62`  
		Last Modified: Wed, 24 Apr 2024 01:53:59 GMT  
		Size: 1.2 MB (1231102 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a63c819b0a54a3439c4d85cae9b15f34d45fc351c7faf6cfbe97152f5da69af3`  
		Last Modified: Wed, 24 Apr 2024 01:53:59 GMT  
		Size: 21.7 KB (21685 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine` - linux; ppc64le

```console
$ docker pull nginx@sha256:d2551f348038d2ea111ba43e8783ddf9ae757cfad1c0d8ffcffe20abccc86897
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.5 MB (20477447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e089772d1f4e8d95970820f8b69676780adb564eeaace4d4d80199b1cd03addc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 17:12:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 16 Apr 2024 17:12:08 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 16 Apr 2024 17:12:08 GMT
ENV PKG_RELEASE=1
# Tue, 16 Apr 2024 17:12:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"74000f32ab250be492a8ae4d408cd63a4c422f4f0af84689973a2844fceeb8a3e7e12b04d7c6dac0f993d7102d920a5f60e6f49be23ce4093f48a8eb1ae36ce5 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 17:12:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Apr 2024 17:12:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Apr 2024 17:12:08 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 16 Apr 2024 17:12:08 GMT
ENV NJS_VERSION=0.8.4
# Tue, 16 Apr 2024 17:12:08 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"74000f32ab250be492a8ae4d408cd63a4c422f4f0af84689973a2844fceeb8a3e7e12b04d7c6dac0f993d7102d920a5f60e6f49be23ce4093f48a8eb1ae36ce5 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0618ea1a358a439e7bcd3ce6d8e3aef7d3c90b908f445905cc43d8b87f081f6f`  
		Last Modified: Wed, 17 Apr 2024 17:19:08 GMT  
		Size: 4.0 MB (4044007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0667d0afb48b224d648771fa7586878061d086b2ef471d1adcec28f08f3945c`  
		Last Modified: Wed, 17 Apr 2024 17:19:07 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e06d36a99e35e11d24638c1bacd84bd3d677e3a71df22e3b5134bf853a5bd87`  
		Last Modified: Wed, 17 Apr 2024 17:19:07 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e426c60c1b32918e2430176b348a76cea83926edf93b970159600de22fd3bd`  
		Last Modified: Wed, 17 Apr 2024 17:19:07 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e921b8ed2c637d3c9d98b8adfd6d750e734471da69b5bfc2bd68c169ff8ec90e`  
		Last Modified: Wed, 17 Apr 2024 17:19:08 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efddf5b0cbfba6813374e9a475908d237f083bbc20645844feb1e47a0dd525c`  
		Last Modified: Wed, 17 Apr 2024 17:19:08 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d25809300478d0ea2d6bbd1d440bd351550ce449be5e48ebffac49b1969f9b1b`  
		Last Modified: Wed, 17 Apr 2024 17:54:02 GMT  
		Size: 13.1 MB (13070504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:27addf0ab6f5f6266b3db6cf4c81b89bc18470d98ab1123f3750dc622f56e25d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1253434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a90e80f69e0ea8e9cdd309e59f2d8d043b155ffe8014a8f8096cefeb57c35dde`

```dockerfile
```

-	Layers:
	-	`sha256:b03ba1814193c79d7f758848021673b63e83c0356b270b94f802fb5979ab4365`  
		Last Modified: Wed, 17 Apr 2024 17:54:01 GMT  
		Size: 1.2 MB (1229273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45cb620e17f440c5773544c4acf6ace31e2d77f1f8cc7aeab0810b4ee7af55fa`  
		Last Modified: Wed, 17 Apr 2024 17:54:01 GMT  
		Size: 24.2 KB (24161 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-alpine` - linux; s390x

```console
$ docker pull nginx@sha256:881fcc30ea2dd8559dbb424b349e0b1860d4321866944f42207a41c98bfb3e72
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20286109 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a046b1b0fdcf5914266494a5c00462a3c65785b3adf158da43e410de16e612d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 16 Apr 2024 17:12:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 16 Apr 2024 17:12:08 GMT
ENV NGINX_VERSION=1.25.5
# Tue, 16 Apr 2024 17:12:08 GMT
ENV PKG_RELEASE=1
# Tue, 16 Apr 2024 17:12:08 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"74000f32ab250be492a8ae4d408cd63a4c422f4f0af84689973a2844fceeb8a3e7e12b04d7c6dac0f993d7102d920a5f60e6f49be23ce4093f48a8eb1ae36ce5 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 16 Apr 2024 17:12:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 16 Apr 2024 17:12:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 16 Apr 2024 17:12:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 16 Apr 2024 17:12:08 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 16 Apr 2024 17:12:08 GMT
ENV NJS_VERSION=0.8.4
# Tue, 16 Apr 2024 17:12:08 GMT
RUN set -x     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-r${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}.${NJS_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 libxslt-dev                 gd-dev                 geoip-dev                 libedit-dev                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"74000f32ab250be492a8ae4d408cd63a4c422f4f0af84689973a2844fceeb8a3e7e12b04d7c6dac0f993d7102d920a5f60e6f49be23ce4093f48a8eb1ae36ce5 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make module-geoip module-image-filter module-njs module-xslt                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -f "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache curl ca-certificates # buildkit
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c285d08a44f13f10d742aed6652649b58908b82b7ba8a7e1e0d48f638b3581b3`  
		Last Modified: Wed, 17 Apr 2024 17:17:18 GMT  
		Size: 4.0 MB (3959367 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d72a7e8bb3aae7e3bf1011dac62abe05cc5e120c5ea4963378bde9a0b6395fd3`  
		Last Modified: Wed, 17 Apr 2024 17:17:18 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73696465c573426465a7bafd35ae6879b567567456a9494094d5af51db5e85c1`  
		Last Modified: Wed, 17 Apr 2024 17:17:18 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdb67b74ee9c6740c1939a32d79091ed3eded6cb636974439f9bdcaa010e0347`  
		Last Modified: Wed, 17 Apr 2024 17:17:18 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92328c99d4566453c50712bc52c3bd739fa2402b92b20be56f14ebf00583a5f9`  
		Last Modified: Wed, 17 Apr 2024 17:17:19 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0105e72b401e654eb331f5d2fc478063e00b4c6a44ba22def43fe313fbc7c618`  
		Last Modified: Wed, 17 Apr 2024 17:17:19 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d224d7c1502ec7bdcf03b9764bcfccc6da387bb815adb4e44acb3df9ae111ecd`  
		Last Modified: Wed, 17 Apr 2024 17:59:59 GMT  
		Size: 13.1 MB (13079521 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-alpine` - unknown; unknown

```console
$ docker pull nginx@sha256:ba3f0fab79dc2b14088ac89368d15f51cd2cd65d482b7cb9063448f1335acaf2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.3 MB (1253284 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c15416df36fbdf472b07a6fbd8bab03e77f340d68ecc8dfa59ae4da1346dd90`

```dockerfile
```

-	Layers:
	-	`sha256:706687290e6df8b9eaf8f2a0a079f8a4839572dd876410c7f2625258c36758ed`  
		Last Modified: Wed, 17 Apr 2024 17:59:58 GMT  
		Size: 1.2 MB (1229203 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4686c0af6d3e340cfe1f6a76c74c4d62cb9d2572743c32fdc1550ba04b306e3`  
		Last Modified: Wed, 17 Apr 2024 17:59:58 GMT  
		Size: 24.1 KB (24081 bytes)  
		MIME: application/vnd.in-toto+json
