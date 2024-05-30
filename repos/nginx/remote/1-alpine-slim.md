## `nginx:1-alpine-slim`

```console
$ docker pull nginx@sha256:89bea3c44e780ff5842200b1002af822f98bd0eaf9207dc221be43ffc460013c
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
$ docker pull nginx@sha256:244d37691a469d45349d9f29e8b7462d9f510b70c0c93acc5d23ee227070c962
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7404445 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df7e0f9c4d6a556a3001a0293f9c77a8b76a1715cea5176d22687cf8881fdf21`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"cd3333f4dfa4a873f6df73dfe24e047adc092d779aefb46577b6307ff0d0125543508694a80158b2bfc891167ad763b0d08287829df9924d4c22f50d063e76c0 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e69ebc7f924a03f4e1d3906db5423920d8b40d8f315db72445e6a7041c6237`  
		Last Modified: Thu, 30 May 2024 15:52:24 GMT  
		Size: 4.0 MB (3991124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628158b45bceaf19d9e86fbfb08c925d75e1e2ab888cd9b97b7c8a8181232be4`  
		Last Modified: Thu, 30 May 2024 15:52:22 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346e52e95fa0a52e495913d9d99e4766d1164631ddbf3a79b1b7860c44a4582a`  
		Last Modified: Thu, 30 May 2024 15:52:24 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c57fb1cd6448c27acb916942fed2522079e5256bc92466c1351f1b6d5f201e9`  
		Last Modified: Thu, 30 May 2024 15:52:24 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc3800d1d0f27990204f4c7f60ef0a8fdbf41a3199d38467475aba551823ccd4`  
		Last Modified: Thu, 30 May 2024 15:52:24 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3227d68030df2f1c6db2654cf30f1e42d5700dc7b5c73eb1a4585bbd588affa`  
		Last Modified: Thu, 30 May 2024 15:52:25 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:5aba8061661e77950bb282888d2739fabd7de620ef3587df47e69580e694904d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.8 KB (869771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b166ea49417584e3c62df17e1d21a8b2d81c4d90e8b627f1431a6fcb84eb18c1`

```dockerfile
```

-	Layers:
	-	`sha256:1b483d4d4d760d0c0620bf8b7311efcd8345d10c2dbf6c3285a28734b340944d`  
		Last Modified: Thu, 30 May 2024 15:52:24 GMT  
		Size: 839.5 KB (839468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a99675d75d6c553975d7232ab73d724b48768743e146441fe03cc9c7fabc7753`  
		Last Modified: Thu, 30 May 2024 15:52:23 GMT  
		Size: 30.3 KB (30303 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:ed62893b3a2ebbd533d8db4b900f3691634f1210b24867d69da6f1a3528a6e60
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6975251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:743ddca613352d271ba52358b40021f6a24f722284bdf83eb8d794f37e40e976`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:17 GMT
ADD file:99cc37cba14ac64dc4652e46dc671888a0265f90992faa05c32d32e21f89c147 in / 
# Fri, 26 Jan 2024 23:49:17 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"cd3333f4dfa4a873f6df73dfe24e047adc092d779aefb46577b6307ff0d0125543508694a80158b2bfc891167ad763b0d08287829df9924d4c22f50d063e76c0 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c35ef88ad30fd0027ecdf5a07da554daea1099b6ccbb4911593dc429cc2b1eb6`  
		Last Modified: Thu, 30 May 2024 15:57:31 GMT  
		Size: 3.8 MB (3805253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30589f30348bcd6c5e77d3fedb7f3906517dd5e4231d90776c0f837b387acfea`  
		Last Modified: Thu, 30 May 2024 15:57:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd715eed8aa3a129ace8df63e69b7bdcc0544ed3819f79ef4c930be692fdd4f0`  
		Last Modified: Thu, 30 May 2024 15:57:31 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d00ea2a6dac2b2eb4bb8c5d9b798a2809a299d9180bc06587cd17e2e03e2b80d`  
		Last Modified: Thu, 30 May 2024 15:57:30 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d20b1665bc2a56011bc9d229ed19e110d0fad9f48c25b19599ab9788efac38`  
		Last Modified: Thu, 30 May 2024 15:57:31 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac79ab8904f186419342b9ec6cb03645472c1e4040d815c831a986c7686bfe87`  
		Last Modified: Thu, 30 May 2024 15:57:31 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:60347540ed7dc3ad802fb435982c056115b175e2814669d10e518fc86a752c66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.2 KB (30202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f116be38ffaaa4bad414cdb33fd6fc4287ecf210e95109aa39af2c4d0ee981b4`

```dockerfile
```

-	Layers:
	-	`sha256:9d812edd5dd39921d73a5aedcaf8f9e52d884a9e237d41a39824df3d26b6b657`  
		Last Modified: Thu, 30 May 2024 15:57:30 GMT  
		Size: 30.2 KB (30202 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:ac6297904fc1a7fa150309938745a5993cbe13859161cbfc18602f0d30c3c2cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6438525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:745a27978104c879560d41e13955fddb2c4809e0930370bc861ca79cb226cc16`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:14:54 GMT
ADD file:dca2a738b46ed78f0ccd7e23ba4d4729528feaa423a0ff0ac5c3512bf43b6fae in / 
# Sat, 27 Jan 2024 00:14:54 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"cd3333f4dfa4a873f6df73dfe24e047adc092d779aefb46577b6307ff0d0125543508694a80158b2bfc891167ad763b0d08287829df9924d4c22f50d063e76c0 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e451de6dc5843d50438edec37f24178df8adbedd7a98ee8912b6fa84907ac42`  
		Last Modified: Thu, 30 May 2024 16:15:27 GMT  
		Size: 3.5 MB (3515020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45c7596ae779d0a727775d1ec9e38811d53f7fb83f71eccbf9d58677175791c8`  
		Last Modified: Thu, 30 May 2024 16:15:26 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41284f149a8bf49454ae7f9e87f090f49fbb16e88e5664922c8eb82405c6c964`  
		Last Modified: Thu, 30 May 2024 16:15:26 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9821b4428c65939dc8f2c8189b7a764ba2ebc5d63552f547a3661618d13ed852`  
		Last Modified: Thu, 30 May 2024 16:15:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f206a9ce8b82d0cba9672d4876361edb5186ef615d6b3a823443a7e9ea9a4323`  
		Last Modified: Thu, 30 May 2024 16:15:27 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40b1d0589dc928e909bb785b9458bfcb0cb2006c0eb226255d6c4ea0c773cafe`  
		Last Modified: Thu, 30 May 2024 16:15:27 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:c61de01689bf52c0a23d9f6fb14ce04596cccef57e5901b3a2c7c220c30fd31d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.0 KB (869973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89cfd06e65a1216bdd279de91230b4adf7e8eafa95a213f9fa1306c01dff88a1`

```dockerfile
```

-	Layers:
	-	`sha256:078748282ed43c14c1f5fd8b2ee8aeee8fab8bd61e55cf04cfa035e6f1dbd740`  
		Last Modified: Thu, 30 May 2024 16:15:27 GMT  
		Size: 839.6 KB (839552 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ad6bb2ff4acc2ffbd4dabab459d2a00b1ea20e01b0c057b78fe705a48fa1bdf9`  
		Last Modified: Thu, 30 May 2024 16:15:26 GMT  
		Size: 30.4 KB (30421 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:d7b293ff0348be8de4be667c82bb5d50a2a264339a2422f76f16d468439731de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7255810 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c84e1e05296a42e4d72aa2441d7c87b3fc45f54d8ec910f3928f425023d558e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:47 GMT
ADD file:d0764a717d1e9d0aff3fa84779b11bfa0afe4430dcb6b46d965b209167639ba0 in / 
# Fri, 26 Jan 2024 23:44:47 GMT
CMD ["/bin/sh"]
# Fri, 03 May 2024 19:49:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 03 May 2024 19:49:21 GMT
ENV NGINX_VERSION=1.25.5
# Fri, 03 May 2024 19:49:21 GMT
ENV PKG_RELEASE=1
# Fri, 03 May 2024 19:49:21 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/27357d6c5453.tar.gz                 && PKGOSSCHECKSUM=\"a80fc5706ad8e98597478b9e041f658375d53d22f7c8004dd16354067a3d48eb4ef234830b697ddf5c45ec57b837237cc11317bcaaa5133ccbe71bce15d969b0 *27357d6c5453.tar.gz\"                 && if [ \"\$(openssl sha512 -r 27357d6c5453.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf 27357d6c5453.tar.gz                 && cd pkg-oss-27357d6c5453                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 03 May 2024 19:49:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 03 May 2024 19:49:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 03 May 2024 19:49:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 03 May 2024 19:49:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:bca4290a96390d7a6fc6f2f9929370d06f8dfcacba591c76e3d5c5044e7f420c`  
		Last Modified: Fri, 26 Jan 2024 23:45:19 GMT  
		Size: 3.3 MB (3347715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddf9db5a05cbf61e62d46b1225986f3238390e770aedf7c3633b0f4984df6a6b`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 3.9 MB (3903507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a83296a673ce8848db1a03260b4104984c299b3619a73842eeecb887e6ebd1c0`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4f3127eb6227853129ee22d81700ccf48bcdcb17929680fc9f01ac3c7bc6dbd`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:166b80e00f74c3a053c98236bd987af4ee91e23276257bf52858ebc900d55bb3`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182e691fb2cc710f857dcd9016d4854cea790a28508e33bf2ef928f61ae6c4d6`  
		Last Modified: Mon, 06 May 2024 21:13:14 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98ff282c446606ae80b6c7812c9248a7b9d56f86b18c0b9b068ba821517cdb66`  
		Last Modified: Mon, 06 May 2024 21:13:14 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b65d384c3f71c738d7e9992279f6fa43a0a8a7feff66e07c6662d186eef702df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.6 KB (869593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18f124044108bd849901878027a9913a737f3768bd84d63c6aa460e0e2b7acdf`

```dockerfile
```

-	Layers:
	-	`sha256:42d1d996c20d556623c0b0768d259bc2ac9f746b08d678e826488644d4e19b8f`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 839.5 KB (839491 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f48abb6517c9a22c329f413775431ead7e736d229353715bfce80de38f88e25`  
		Last Modified: Mon, 06 May 2024 21:13:13 GMT  
		Size: 30.1 KB (30102 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:0f0e4c1c1f96deb367cf4c2432d7bc6826048af0ce079b11f577121067881ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7266732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f1fee51ca9d76b66f2f99c2d2d0c57925e673c04e988568d04dd813a959ff1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:19 GMT
ADD file:50130ffc87b68d2889c28269d2783e37c42087ce4793108222ad53ed22443a90 in / 
# Sat, 27 Jan 2024 00:38:19 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"cd3333f4dfa4a873f6df73dfe24e047adc092d779aefb46577b6307ff0d0125543508694a80158b2bfc891167ad763b0d08287829df9924d4c22f50d063e76c0 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f03dacea07ad9ac25f469ebf7e4ecb0dea6eb574a9e4c3f9e2e9c2c89cb7e8e7`  
		Last Modified: Thu, 30 May 2024 15:54:00 GMT  
		Size: 4.0 MB (4018045 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628158b45bceaf19d9e86fbfb08c925d75e1e2ab888cd9b97b7c8a8181232be4`  
		Last Modified: Thu, 30 May 2024 15:52:22 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b850dbedbb96d310ceb9437fad7c55ee6512eb3c25911c867e6b10b445c03c4`  
		Last Modified: Thu, 30 May 2024 15:54:00 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8abd8ed0ca57229ffa1d47161963f992adbc0d1d7934bae20433b9fa9faa9bf7`  
		Last Modified: Thu, 30 May 2024 15:54:00 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6269989ef7271e0042d41d27af1f4ccd720004ee39dec4761e8221af89a65016`  
		Last Modified: Thu, 30 May 2024 15:54:00 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c5833fad6c79a19ce3ee11f61e4accb6bdc67386f0be087f0cb16d1f3adfbc`  
		Last Modified: Thu, 30 May 2024 15:54:01 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:0ca612617b77bf9bf07ac7a715a413688a4a76781a476970cefff99de2be1dfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **869.7 KB (869657 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f055782d03a2809f6e0a7256cadf88785000343de4e7f72ddd811a0788fd3874`

```dockerfile
```

-	Layers:
	-	`sha256:4df27fc7ad9d1428bd3c87309405a8dc1ca9dd80ce0997de44912577ba085624`  
		Last Modified: Thu, 30 May 2024 15:54:00 GMT  
		Size: 839.4 KB (839413 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:30b223f15c4dab3424905d20edc1754c92db0546e037c6d143553e83adfa2c22`  
		Last Modified: Thu, 30 May 2024 15:54:00 GMT  
		Size: 30.2 KB (30244 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:0f368dbe2d0bf5bf8face77bdd5e29e7a537f03110058b01b86e5e77e831f284
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7410231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617f904e18563a6eba742455b26bb5eabefb9be239ca618bcf080361b302f901`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"cd3333f4dfa4a873f6df73dfe24e047adc092d779aefb46577b6307ff0d0125543508694a80158b2bfc891167ad763b0d08287829df9924d4c22f50d063e76c0 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2e235e9ec090a6406602d09e30d9b047d7ed950c15fce962c61567bba9307fb`  
		Last Modified: Thu, 30 May 2024 16:18:30 GMT  
		Size: 4.0 MB (4047273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05fdb5df5a0aeefb50c79e44df9fafc2dd6fce32a2661b882991bb39c8d5b54a`  
		Last Modified: Thu, 30 May 2024 16:18:29 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d758452207a56c268af1f43cba3caa5f44cd19fd2cb855902976c81741b2ccb1`  
		Last Modified: Thu, 30 May 2024 16:18:29 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c5e826c9c7729f3c8732a6e055a8e9074945f7ce5766fad4dc3c3c03978b36a`  
		Last Modified: Thu, 30 May 2024 16:18:29 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d268eb649bda76f7bb048db01b45204b190ad4fc4c0188e4503f23c3201f6921`  
		Last Modified: Thu, 30 May 2024 16:18:30 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3990c421aeae9132280423f12522a379b26f1ae6d6d3558bd2a78f1c69966c1`  
		Last Modified: Thu, 30 May 2024 16:18:30 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:a0c513910662889dd0366655d9cd24bbee077b120ce5a5aa0c340a58b2890c64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **868.0 KB (867961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b65cdc2372a7b3628540dbb833339afe1b7ad16fc4ff3da74d53b15ea3f1ea6`

```dockerfile
```

-	Layers:
	-	`sha256:2c48256616313297753a3ddaa78616832839cd0c78fbc4939ed69e1ea6d1de8f`  
		Last Modified: Thu, 30 May 2024 16:18:30 GMT  
		Size: 837.6 KB (837584 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d53f0dc11973bb465956a5dab0605bbd7c3b45bc6c424b5afd4cf353cf51c955`  
		Last Modified: Thu, 30 May 2024 16:18:29 GMT  
		Size: 30.4 KB (30377 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:5f10b3f510518c32daee990ab392e137e7469635363caee81fbff8d6b18ff8a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7210209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70abef9b8429dc6b6eb01dfa32ecae69e550b52a50f1935927ce596d2c07666c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/mainline/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"cd3333f4dfa4a873f6df73dfe24e047adc092d779aefb46577b6307ff0d0125543508694a80158b2bfc891167ad763b0d08287829df9924d4c22f50d063e76c0 *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 29 May 2024 23:55:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 29 May 2024 23:55:01 GMT
EXPOSE map[80/tcp:{}]
# Wed, 29 May 2024 23:55:01 GMT
STOPSIGNAL SIGQUIT
# Wed, 29 May 2024 23:55:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9689919c8c3fe8e490cdd30b0f55915474e8bce691e8aee3df93af3294699a1d`  
		Last Modified: Thu, 30 May 2024 16:14:28 GMT  
		Size: 4.0 MB (3962969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3a75af822b76394bd45ac79fbc0328c03a5ee4a3cdcdfb2857a6f8e27f10bbb`  
		Last Modified: Thu, 30 May 2024 16:14:27 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a35229078a4abd10839ccf1c8162bb91751882eb2f5813eb5121f20456a1bac`  
		Last Modified: Thu, 30 May 2024 16:14:27 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8585bbabc773a4dd71d2f0e96ffe5d7c01443e5e37cb0338b4e84c5764312ad3`  
		Last Modified: Thu, 30 May 2024 16:14:27 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d68db2790c8017096a0dafa76d037fe59016b80e4492b6b4284b247ee511d1c3`  
		Last Modified: Thu, 30 May 2024 16:14:28 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ee8f67942b6f430d966da07dbb7cbdcd59b28aa3602b0e5555a6535f44513bc`  
		Last Modified: Thu, 30 May 2024 16:14:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:4ba1264ff2e9e4461dcaf779cea262facb51da0cd0930c07ebe0401851c1aef7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79bebee243fb8c099e95153df9a2c40182e9be2a5dca14d8ab393ef541e8de5a`

```dockerfile
```

-	Layers:
	-	`sha256:7f2a20479bce308c1f4ab3db619678c8b1c0e03c41520df6b5eccc21c886a4e0`  
		Last Modified: Thu, 30 May 2024 16:14:28 GMT  
		Size: 837.5 KB (837514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:299721b90876e65be8e3c18a8fc3ae12644b1ea87c898903c45fd86ee8d7b479`  
		Last Modified: Thu, 30 May 2024 16:14:27 GMT  
		Size: 30.3 KB (30303 bytes)  
		MIME: application/vnd.in-toto+json
