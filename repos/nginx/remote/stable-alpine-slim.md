## `nginx:stable-alpine-slim`

```console
$ docker pull nginx@sha256:caaa51cbb24b1d2e9a0cb41e4f38c28b15f83ba7e396438f5353589606d4aa9a
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

### `nginx:stable-alpine-slim` - linux; amd64

```console
$ docker pull nginx@sha256:59e2722d3aac2a84468c4b63b7f3cecd8820849f86f1afa7efff53caeaf3176b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7398695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6480310617dbbdd6332029ed897515097504f8c42849dccb5f8a52d608e37187`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:48 GMT
ADD file:37a76ec18f9887751cd8473744917d08b7431fc4085097bb6a09d81b41775473 in / 
# Sat, 27 Jan 2024 00:30:48 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:4abcf20661432fb2d719aaf90656f55c287f8ca915dc1c92ec14ff61e67fbaf8`  
		Last Modified: Sat, 27 Jan 2024 00:31:24 GMT  
		Size: 3.4 MB (3408729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091275ae680776b2922329c9b3f581863a6de95856c04671e8f4dffb8c7578ca`  
		Last Modified: Wed, 24 Apr 2024 00:51:32 GMT  
		Size: 4.0 MB (3985376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680080a33f4ff2b0d8aedac2d12fda4dec7b4522728f1bc522d45c4c871de011`  
		Last Modified: Wed, 24 Apr 2024 00:51:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04f45f24a9c66d04eee91e92f732179b6f37f834b8751f158a96f479a02138c`  
		Last Modified: Wed, 24 Apr 2024 00:51:32 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26087820d60a54635a5c91a255fc080b80bb15c40b880e2441dcf410d2b908f7`  
		Last Modified: Wed, 24 Apr 2024 00:51:32 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd75bb60cdbb992a9f78232b550adf88b3199f1c8853d36939eb9cd1922fa31f`  
		Last Modified: Wed, 24 Apr 2024 00:51:32 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125d178ee43c0b386693c2635ecce90f8aad572f9a7a05f18ba66fef827d089c`  
		Last Modified: Wed, 24 Apr 2024 00:51:33 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:7227320bc965ecfda374cbb49f3ccacde0693e22c2ac7606d9c50d280d514748
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.4 KB (867398 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089210973ad18b6a8fcddabe724ab4b749c66f33f45b0f320f1fe634bc21512b`

```dockerfile
```

-	Layers:
	-	`sha256:e6ed98e78d0d9d8729a81d64a897cfec29c3a55cbf6720e8ba7746f70fee076c`  
		Last Modified: Wed, 24 Apr 2024 00:51:32 GMT  
		Size: 838.2 KB (838212 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b8dfb6a4c9cf482836ca3d9be561ce580edeb5c07bf7e8430979163f4f117b`  
		Last Modified: Wed, 24 Apr 2024 00:51:32 GMT  
		Size: 29.2 KB (29186 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm variant v6

```console
$ docker pull nginx@sha256:1267f3d1e406487e189115a59c00d950ce30b98f27fafbb4941cf37acb854564
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.0 MB (6971184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca63ea52f28dd5b1795ee8967df705bbc769303a93e173d09d50155e02c833d`
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
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:0dc2e6c0f9ded2daeca96bbf270526d182d2f4267f5c7610c222c05cad6f6b96`  
		Last Modified: Fri, 26 Jan 2024 23:49:40 GMT  
		Size: 3.2 MB (3165396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f16a125c59f6eca81c0abe2c1109a15596d7cb3b69e1d8eb88df96e1cb08f65`  
		Last Modified: Wed, 24 Apr 2024 01:04:04 GMT  
		Size: 3.8 MB (3801210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51f589f70383a842a291c029828ff223dd089d564568711aa36acaff840dd042`  
		Last Modified: Wed, 24 Apr 2024 01:04:04 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecaba49f1f8d1d710aa3c9e2bff7f8de6cb418583aabb24ad81201074882b5da`  
		Last Modified: Wed, 24 Apr 2024 01:04:04 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:666b09b5967a407eee680e5001d0f1347388fdd5539713fbad2f1e0cca532677`  
		Last Modified: Wed, 24 Apr 2024 01:04:04 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbd5153f49bab3f8becd3f036188d70a9e48eafea4d010a563fcff7679a38997`  
		Last Modified: Wed, 24 Apr 2024 01:04:05 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f02685bdaa646292062ec69c242f035141c5b52fcdb1de26eb6a8d520db77d`  
		Last Modified: Wed, 24 Apr 2024 01:04:05 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:55313604f45cc2580178620ab51686c3f2b3145d3c974de2f017897ae995b774
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.9 KB (28887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c48f4d45f6937232690cf1e1a2a26ddc4f633014e1e9f9800329b9d3968dff82`

```dockerfile
```

-	Layers:
	-	`sha256:37730b7f3a29a2cada59b112f793bfff968f271b010eb4f52b41c509e960e8e3`  
		Last Modified: Wed, 24 Apr 2024 01:04:04 GMT  
		Size: 28.9 KB (28887 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b7987ff9726d581cfd8c25833232335e991595a816410f31028fce3e5119d111
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 MB (6436409 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b7bb898780c4a2b2eb6e85d67048dd7713255450ad154d556a9f29dabefbfc`
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
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:fda0ff469afd28d9cfbb946e8e0a3c911c591a2691bea62be9187e45a1c50549`  
		Last Modified: Sat, 27 Jan 2024 00:15:27 GMT  
		Size: 2.9 MB (2918899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdf02467fad3468c99d6c553f7b0c6b0af9c44ca2e7cac3d7097f8f822f359e1`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 3.5 MB (3512920 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:143f2cc87ddbf7a232207e3bf45ac9d169dec50fa16ea3d3b65c104c610d49c4`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2b227bb717a95e2bccd3c15c8b21fee8aca7cd6c4d92cec52add755643ee692`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:693ba1e2ad342ea823fc614668a786c150c22af88d3c95e6fcc93e3fd109a416`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277c514996771d85afc4209ad07d64b250abbbe2e47091008f3c3773e8e6f327`  
		Last Modified: Wed, 24 Apr 2024 01:30:57 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a85c080e146e6a089a17992d285560081f469a8cb27723f2cdbb70ef837fd39`  
		Last Modified: Wed, 24 Apr 2024 01:30:57 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:5799341a5a4a29d2fde85c19d6c0d4075f1fbfbbcd767509c6cde517c7d35bb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.4 KB (867370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab8cc3da67e420466f29bd1626b0cfeabdf4ab49e5e0c33c3ce35af618608f4`

```dockerfile
```

-	Layers:
	-	`sha256:00dc0ebcda67c05ded891b328946a5bb9c826ed1660b46988a51c6cb103b2daa`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 838.3 KB (838264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b15f7ce1b658fa7d394caf07b05c1627f1889458878860826470337d907dff4c`  
		Last Modified: Wed, 24 Apr 2024 01:30:56 GMT  
		Size: 29.1 KB (29106 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:dff63515ad582e300f4efa0ff5357bd6e593abb53a2d086e66362e8468fe81a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.0 MB (5048615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2d16221207d045c153407c4b180682c57c6fc957dfa15f949094f4cacdd9e32`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 11 Apr 2023 19:57:20 GMT
ADD file:c3b6b575eb741f914ec12bd4df43de0cb044a1f2bae7ff15d176e49b5986d903 in / 
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["/bin/sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 11 Apr 2023 19:57:20 GMT
ENV NGINX_VERSION=1.24.0
# Tue, 11 Apr 2023 19:57:20 GMT
ENV PKG_RELEASE=1
# Tue, 11 Apr 2023 19:57:20 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"dc47dbaeb1c0874b264d34ddfec40e7d2b814e7db48d144e12d5991c743ef5fcf780ecbab72324e562dd84bb9c0e4dd71d14850b20ceaf470c46f8fe7510275b *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -n "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && if [ -n "/etc/apk/keys/nginx_signing.rsa.pub" ]; then rm -f /etc/apk/keys/nginx_signing.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 11 Apr 2023 19:57:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 11 Apr 2023 19:57:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 11 Apr 2023 19:57:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 11 Apr 2023 19:57:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:5385a9a590c3e2872b3ed27554a56fb7ce544c694b41b9b95d70fa86f30b0566`  
		Last Modified: Fri, 26 Jan 2024 23:45:40 GMT  
		Size: 3.3 MB (3258283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af2cabb588b4b69717ea53c4dd367a1520ebc85ca22dc03bc14e5174f3a0314c`  
		Last Modified: Sat, 16 Mar 2024 15:48:32 GMT  
		Size: 1.8 MB (1786582 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb38e42d8990cf14b87a3189a04b629370d251b0d09a9b88cfb383c1ec7236ef`  
		Last Modified: Sat, 16 Mar 2024 15:48:31 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572477dc8cc340b1c1723b964a396d2dbb23a3c751315a5bb3319a8ed46eeb56`  
		Last Modified: Sat, 16 Mar 2024 15:48:31 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1af48caa863fda86bba54f943f58775b7a1373624ed2c48f85e1173914d3160`  
		Last Modified: Sat, 16 Mar 2024 15:48:31 GMT  
		Size: 769.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e396540ae07eaf3853db78848913703f40cad35739b74e44e0b196cdaf8fb3`  
		Last Modified: Sat, 16 Mar 2024 15:48:32 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:221d750a3574890cf6a20ed9e0732968be61b4bfc5ebe5b004502ceeb7e015d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **864.7 KB (864673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9554293ab03823f9678b8503271f911fdc88048b83068388636a843606370e1d`

```dockerfile
```

-	Layers:
	-	`sha256:ca8461548f63d7617f7c46f27ea26615496caafcf94b31c1b6d98213f64f40a7`  
		Last Modified: Sat, 16 Mar 2024 15:48:31 GMT  
		Size: 837.0 KB (836965 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b669855934ffc87226e050bf7b918507fc5adfc89327cb491ffacdebf4c0bc4`  
		Last Modified: Sat, 16 Mar 2024 15:48:31 GMT  
		Size: 27.7 KB (27708 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; 386

```console
$ docker pull nginx@sha256:47dded0b02e180ea54f935fc736411e41fd5135f1c20f78627119bdd419d990f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.3 MB (7262352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c14b880b7e561841a966400bfb95a6398a66709f86e7b3ee0827f5eb0102b6`
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
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:4a0759b5afbffdc507fbb4e32b3a139063c3a5c0829f811973850447f98830ae`  
		Last Modified: Sat, 27 Jan 2024 00:38:47 GMT  
		Size: 3.2 MB (3244089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5295af929dff864ba14a6caa6d66b49dbdfff7fd8008b30707913e81e7c1af`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 4.0 MB (4013680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29e0a79bac2e686da94a3ba97eb832086ae38edf55382a500bb2619a134efb97`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d346e21a2e61ebf194bf24a99af5c9595b5d8eba1e0a65140d48f575fb7c659`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37ccda82465578abea36f35f61c44a4545792454f8ec8d756a3af6e87b9b08b7`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c22f0cf5e27a7ec02821aa47edbed9115917c212bd7b0fb7aaff6ce872c4240`  
		Last Modified: Wed, 24 Apr 2024 00:52:21 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1aa24a77b2746d7212db2570317b441fd4aa85e64ff41d3a5c35afa4ca2071a`  
		Last Modified: Wed, 24 Apr 2024 00:52:21 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:9bb78be8ab73cc333bd067c9339d04328da7362a5f7ba2a06481fdd9cd738ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.3 KB (867324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b96970a96e50d35590a7319baf3328629373e5d8263a0ae1759bd7bc24901eb`

```dockerfile
```

-	Layers:
	-	`sha256:40f169ca7ab77da6eb27b109a30bc89da817614138b811b203c89d14976994dd`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 838.2 KB (838177 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c14fd7a65fc5fc741c488f35db2beadb61c43cfcebf4b77098c8d08488d5998d`  
		Last Modified: Wed, 24 Apr 2024 00:52:20 GMT  
		Size: 29.1 KB (29147 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; ppc64le

```console
$ docker pull nginx@sha256:e4c607f0df3f73517dbbc1188f9ff099367eedc26332e4b829b0818093d7e896
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.4 MB (7407043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8276af0c6fe7e77276fac0319e02fb827b285dcb13b822dab1f9150e00000ff0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:35 GMT
ADD file:76976bd619bf0c4e63bbd1d1d0a20b224d1f14070cb9be6036c1b7672a7848ba in / 
# Sat, 27 Jan 2024 00:27:35 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:f4968021da4ff8b74325e5aebf0f9448b44becfdd14df80ecba474e43cc92546`  
		Last Modified: Sat, 27 Jan 2024 00:28:10 GMT  
		Size: 3.4 MB (3358353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5842680d7bb2e7e5a243413e13113582352e3da959b9ceb824bba7d327ef99a7`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 4.0 MB (4044107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86ff777fc13b28a36f88ef42d61af715184659340e80729633e0c212758a1621`  
		Last Modified: Wed, 24 Apr 2024 01:47:39 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89f5f7179c98fc0e8f482a5b9a085ad8967d9691077b70ea075d3ae1511683a2`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e2828c9c8f9b99633201aa78a8c68ee15a739e80b97a77544d5341296aad317`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0fe46d9fe812b55f7ed6e7ada3aeb08825a9609ededd03eafbe3392f8a8f658`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f49548c9348f9487c118e382ebd22cce9a995c68c74c529a1e3761f2eae3abd`  
		Last Modified: Wed, 24 Apr 2024 01:47:41 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:b3a1704f24b2f1c076d20350e3d359e7417a86f7d01ad01392322fc54865a6c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.4 KB (865374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29d3f0b9a5ba75d55ffed3d3c9c19af6599c3656ad3486aa6d43ee88a8e115ca`

```dockerfile
```

-	Layers:
	-	`sha256:79184418e2cd00e9bdcfc2cd235ecd65641a593da576f97b5082e9459504a174`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 836.3 KB (836304 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e75b619617db03e06bc9bc6d17f58585ee9b55c52fd7f77c49dd84897e149538`  
		Last Modified: Wed, 24 Apr 2024 01:47:40 GMT  
		Size: 29.1 KB (29070 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-alpine-slim` - linux; s390x

```console
$ docker pull nginx@sha256:bf950a3c17c4c0648acace1637f7caf1d8cb0b157d42f7dc18a21d9fdd39922b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.2 MB (7206575 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ac1012f5dc7e25fabbd4c19549374c32d7e78fe158a89df6ba8d44d08365604`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Sat, 27 Jan 2024 00:37:52 GMT
ADD file:a3a70231936c63931e39d0cbee91dc800a1f64c713d03da79c5cc7b7d68bde92 in / 
# Sat, 27 Jan 2024 00:37:52 GMT
CMD ["/bin/sh"]
# Tue, 23 Apr 2024 21:35:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 23 Apr 2024 21:35:33 GMT
ENV NGINX_VERSION=1.26.0
# Tue, 23 Apr 2024 21:35:33 GMT
ENV PKG_RELEASE=1
# Tue, 23 Apr 2024 21:35:33 GMT
RUN set -x     && addgroup -g 101 -S nginx     && adduser -S -D -H -u 101 -h /var/cache/nginx -s /sbin/nologin -G nginx -g nginx nginx     && apkArch="$(cat /etc/apk/arch)"     && nginxPackages="         nginx=${NGINX_VERSION}-r${PKG_RELEASE}     "     && apk add --no-cache --virtual .checksum-deps         openssl     && case "$apkArch" in         x86_64|aarch64)             set -x             && KEY_SHA512="e09fa32f0a0eab2b879ccbbc4d0e4fb9751486eedda75e35fac65802cc9faa266425edf83e261137a2f4d16281ce2c1a5f4502930fe75154723da014214f0655"             && wget -O /tmp/nginx_signing.rsa.pub https://nginx.org/keys/nginx_signing.rsa.pub             && if echo "$KEY_SHA512 */tmp/nginx_signing.rsa.pub" | sha512sum -c -; then                 echo "key verification succeeded!";                 mv /tmp/nginx_signing.rsa.pub /etc/apk/keys/;             else                 echo "key verification failed!";                 exit 1;             fi             && apk add -X "https://nginx.org/packages/alpine/v$(egrep -o '^[0-9]+\.[0-9]+' /etc/alpine-release)/main" --no-cache $nginxPackages             ;;         *)             set -x             && tempDir="$(mktemp -d)"             && chown nobody:nobody $tempDir             && apk add --no-cache --virtual .build-deps                 gcc                 libc-dev                 make                 openssl-dev                 pcre2-dev                 zlib-dev                 linux-headers                 bash                 alpine-sdk                 findutils             && su nobody -s /bin/sh -c "                 export HOME=${tempDir}                 && cd ${tempDir}                 && curl -f -O https://hg.nginx.org/pkg-oss/archive/${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && PKGOSSCHECKSUM=\"f0ee7cef9a6e4aa1923177eb2782577ce61837c22c59bd0c3bd027a0a4dc3a3cdc4a16e95480a075bdee32ae59c0c6385dfadb971f93931fea84976c4a21fceb *${NGINX_VERSION}-${PKG_RELEASE}.tar.gz\"                 && if [ \"\$(openssl sha512 -r ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz)\" = \"\$PKGOSSCHECKSUM\" ]; then                     echo \"pkg-oss tarball checksum verification succeeded!\";                 else                     echo \"pkg-oss tarball checksum verification failed!\";                     exit 1;                 fi                 && tar xzvf ${NGINX_VERSION}-${PKG_RELEASE}.tar.gz                 && cd pkg-oss-${NGINX_VERSION}-${PKG_RELEASE}                 && cd alpine                 && make base                 && apk index -o ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz ${tempDir}/packages/alpine/${apkArch}/*.apk                 && abuild-sign -k ${tempDir}/.abuild/abuild-key.rsa ${tempDir}/packages/alpine/${apkArch}/APKINDEX.tar.gz                 "             && cp ${tempDir}/.abuild/abuild-key.rsa.pub /etc/apk/keys/             && apk del --no-network .build-deps             && apk add -X ${tempDir}/packages/alpine/ --no-cache $nginxPackages             ;;     esac     && apk del --no-network .checksum-deps     && if [ -n "$tempDir" ]; then rm -rf "$tempDir"; fi     && if [ -f "/etc/apk/keys/abuild-key.rsa.pub" ]; then rm -f /etc/apk/keys/abuild-key.rsa.pub; fi     && apk add --no-cache --virtual .gettext gettext     && mv /usr/bin/envsubst /tmp/         && runDeps="$(         scanelf --needed --nobanner /tmp/envsubst             | awk '{ gsub(/,/, "\nso:", $2); print "so:" $2 }'             | sort -u             | xargs -r apk info --installed             | sort -u     )"     && apk add --no-cache $runDeps     && apk del --no-network .gettext     && mv /tmp/envsubst /usr/local/bin/     && apk add --no-cache tzdata     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:eb8fba61d86413beda3240c40c599041e040e658cd8314e38ee15e67ea57d349`  
		Last Modified: Sat, 27 Jan 2024 00:43:21 GMT  
		Size: 3.2 MB (3242635 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8d94a7e88836152f6e5ef2857a7c6d914ba17974891424e7d1ca48e44618af3`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 4.0 MB (3959358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:043a951cb40a3a3a8eb67555bc9127380b5d6d8649f71be69b1356340fdf0f7d`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81834bfd250003c18f8a15c0799a1c354a4dcf4018f23ba960a8217ad428cf7a`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ce4a4c046e97fb7083c5938ab708890488eca1189a981f32c5951a30953382`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b6890302afab99fa6316e89cc4e8fc2a7841e7a617b656c6c2989bb67179f94`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8135d2eb47d1611822918bbdf0683a72705af33764ddb656b10909ee54bcfcb6`  
		Last Modified: Wed, 24 Apr 2024 02:09:12 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-alpine-slim` - unknown; unknown

```console
$ docker pull nginx@sha256:86abe134bbd2887d6efcf5d51d3c4fd8571d17bd6bb8bb899ec6649ebdf90c33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **865.3 KB (865278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ef44c75e146c4e7953b4f0014739c6c1d8c047da35ceea60a702f89568cb14a`

```dockerfile
```

-	Layers:
	-	`sha256:e80812785a74c33f1b33ae4304b75c96f7c5c3dd67950486bd0ce26e42df7512`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 836.3 KB (836258 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:476381bb92f116881abc90152414de38752f71f1862ed2c68006868598bbdb84`  
		Last Modified: Wed, 24 Apr 2024 02:09:11 GMT  
		Size: 29.0 KB (29020 bytes)  
		MIME: application/vnd.in-toto+json
