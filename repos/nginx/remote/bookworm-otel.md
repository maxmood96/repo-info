## `nginx:bookworm-otel`

```console
$ docker pull nginx@sha256:a527db58c842acc6e293d59b966d50999b5198d0c0b052fa97a0b17b0cd39c09
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:bookworm-otel` - linux; amd64

```console
$ docker pull nginx@sha256:e0630073fb48516327a98a1bf5837c0150f200ee11ddbab7f180820c859eeb89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73945919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd039c8268f75774070a8922ada3ed99df5872044768c88d98097acbd89450ec`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 29 May 2024 23:55:01 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Wed, 29 May 2024 23:55:01 GMT
CMD ["bash"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_VERSION=0.8.4
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_RELEASE=2~bookworm
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2~bookworm
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
# Wed, 29 May 2024 23:55:01 GMT
ENV OTEL_VERSION=0.1.0
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b156574604a095a5847d3b34cf36d484bb49862365e996b391d0ba0f345034`  
		Last Modified: Tue, 02 Jul 2024 03:20:19 GMT  
		Size: 41.8 MB (41833344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea5d7144c337402f813ea7c05c11dab58b7841f4c41fb5f5058abefbc2451ec5`  
		Last Modified: Tue, 02 Jul 2024 03:20:18 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bbcb9df2c93e03db739f7e49ce73eda0325b8087ef8e88386d303d883c357ab`  
		Last Modified: Tue, 02 Jul 2024 03:20:18 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537a6cfe3404285310129c72dfc3f352e7c5db1a5f296e514d739322bab5a998`  
		Last Modified: Tue, 02 Jul 2024 03:20:18 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767bff2cc03ef46478039907c5bca487eb27d5f43a38571985e4ed4dc0403d5a`  
		Last Modified: Tue, 02 Jul 2024 03:20:19 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adc73cb74f2591613c7c88f7f6a313c3373bbfa3bda0983677bb233668b4033a`  
		Last Modified: Tue, 02 Jul 2024 03:20:19 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c49868ad78a736b7be884be011c2454ed098007400ef4b4da2963b225180fd7b`  
		Last Modified: Tue, 02 Jul 2024 04:10:07 GMT  
		Size: 3.0 MB (2981714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:44705f4f943ead9772d4843f2046497bb27cea93732800932aa153864336b1bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2938363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93050243b7f7458826bfcf6ab68646d08ac54d2e7783d04e73419e9689bb4b70`

```dockerfile
```

-	Layers:
	-	`sha256:bdfdf2d84badf2f99d1f462fbe33cfe6b83e1557f914b712012529050bc09236`  
		Last Modified: Tue, 02 Jul 2024 04:10:07 GMT  
		Size: 2.9 MB (2917506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9260cda91f99e9d5a132aeaa6e8f58ff084dabb7c2cb8f5ffc9cc7b44809fada`  
		Last Modified: Tue, 02 Jul 2024 04:10:06 GMT  
		Size: 20.9 KB (20857 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:bookworm-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:da6bf9a365a5dd404abdf396f6d34efa0940eea0b37c11e8c76be10b31c02eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70472196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67b2207e73405d6911bba1baaf4876d090f55a40c7a229e2ca88a5e8cff6b401`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 29 May 2024 23:55:01 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
# Wed, 29 May 2024 23:55:01 GMT
CMD ["bash"]
# Wed, 29 May 2024 23:55:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 29 May 2024 23:55:01 GMT
ENV NGINX_VERSION=1.27.0
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_VERSION=0.8.4
# Wed, 29 May 2024 23:55:01 GMT
ENV NJS_RELEASE=2~bookworm
# Wed, 29 May 2024 23:55:01 GMT
ENV PKG_RELEASE=2~bookworm
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
# Wed, 29 May 2024 23:55:01 GMT
ENV OTEL_VERSION=0.1.0
# Wed, 29 May 2024 23:55:01 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e29cef1068774f811cf4f4cc27bc25288de2961a4b71f407c7308b8fcfa3b116`  
		Last Modified: Tue, 02 Jul 2024 16:04:06 GMT  
		Size: 38.5 MB (38465973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9bf20d5335e3b7521df92e13e0922b2eeb4122ae43428807b8e7095e2dea418`  
		Last Modified: Tue, 02 Jul 2024 16:04:04 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1394e86b8f584a68a57cf6da2981896cc42386a5502aa0405adb398af30eba2e`  
		Last Modified: Tue, 02 Jul 2024 16:04:04 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b2b3e0f512f898c91ca134f4b49c3f49434f945ac79b02a01bfd3d0f4d40370`  
		Last Modified: Tue, 02 Jul 2024 16:04:05 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a11b5a77155d55adc4a1d97469f7425e28c208911c2584e10a0bbec969b775d`  
		Last Modified: Tue, 02 Jul 2024 16:04:05 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb6d6e4aad9ce40369e91944e979a301800dec8b85ed02cfb13917a2d807e17f`  
		Last Modified: Tue, 02 Jul 2024 16:04:05 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53dd02e4d7cb186ca2cac4e2a57952b14f728c58864fb3c125b8217e7ba59655`  
		Last Modified: Wed, 03 Jul 2024 01:56:16 GMT  
		Size: 2.8 MB (2845076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:bookworm-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:a276739fd92b5c3c732550428388367cfd7ef6da10c200eef8bc01e29504cbf3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2939283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2316cea4521d15e60d9408b851e559117fefbb1f2b4c5ba9c61ddeed2c6ff5b2`

```dockerfile
```

-	Layers:
	-	`sha256:2012e29f1db2094f0e237708f8e58f90cdf73c4e8cb9f0cb73b807731c7df120`  
		Last Modified: Wed, 03 Jul 2024 01:56:16 GMT  
		Size: 2.9 MB (2917957 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1492ff0f57ecbc35b2910af846dea9db1055af95b69276c74a26306657afe1a7`  
		Last Modified: Wed, 03 Jul 2024 01:56:16 GMT  
		Size: 21.3 KB (21326 bytes)  
		MIME: application/vnd.in-toto+json
