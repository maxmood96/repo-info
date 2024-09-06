## `nginx:1-otel`

```console
$ docker pull nginx@sha256:2668f79cfaf122f99448b34669e880aa83d7898e75b8f416b0e1c9ee23ed21b0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `nginx:1-otel` - linux; amd64

```console
$ docker pull nginx@sha256:09ce6fa56a6406bb5cf9b06ced796a9be3955d22fa522c571eecf9f05a17556d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (73989440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:098a4aad8881a6a18a55956c38cd2649d9aef539f5612f3e045d69fd87c5f306`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:d13afefcc2b0b02b598a3ac2598fe2187db41de1e17820e5b600a955b1429d59 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.27.1
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 21:31:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 21:31:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 21:31:12 GMT
ENV OTEL_VERSION=0.1.0
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:a2318d6c47ec9cac5acc500c47c79602bcf953cec711a18bc898911a0984365b`  
		Last Modified: Wed, 04 Sep 2024 22:34:17 GMT  
		Size: 29.1 MB (29126484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:095d327c79ae6eb03406dd754eb917fbe7009c6a9aa6c0db558f9dea599db8ea`  
		Last Modified: Wed, 04 Sep 2024 23:11:14 GMT  
		Size: 41.9 MB (41876592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbfaa25db775e54ec75dabe7986451cb99911b082d63bbf983ab20fc6f7faaf4`  
		Last Modified: Wed, 04 Sep 2024 23:11:13 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb6fb0cfb2b319dee79e476c11620e7fa47f22ecdedc999e207984f62a4554c`  
		Last Modified: Wed, 04 Sep 2024 23:11:13 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0723edc10c178df9245f49c9b8e503c4223a959ee5a072f043d71669132bc5e9`  
		Last Modified: Wed, 04 Sep 2024 23:11:13 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24b3fdc4d1e3b419643068364b3d4e1b7e280f5a8a3c1e3651e9e67363e6434b`  
		Last Modified: Wed, 04 Sep 2024 23:11:14 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3122471704d5d924d1f7daac334252487e3c35bfb23163b840954aff355c4a6b`  
		Last Modified: Wed, 04 Sep 2024 23:11:14 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d27c867c9d0d6ec03d75b6191aaaf9bc0823ce1a7193321e050b20d047187e8d`  
		Last Modified: Thu, 05 Sep 2024 00:15:32 GMT  
		Size: 3.0 MB (2981776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:0f5614ac6c71d1b07ccd4d48b98b104baa70aae215581464854ef3f05a2fd911
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a2dc57c858ce8b1e1174a5cf38ea2cfb590acfcef928094adb81e7a7163092b`

```dockerfile
```

-	Layers:
	-	`sha256:9755b5ba37a7e5246441d73edaa2c0de648fa591d4c67eb78a8922c1b6d24354`  
		Last Modified: Thu, 05 Sep 2024 00:15:32 GMT  
		Size: 3.0 MB (2951232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45b9952f25f23e7db30db3a4dfe56dab29c3266b8f4004c00544c51051b23795`  
		Last Modified: Thu, 05 Sep 2024 00:15:31 GMT  
		Size: 20.9 KB (20905 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-otel` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:2b55555559c2978f236489db500c61962155b717da3ef64ef6db63e457bc1466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70520157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e8f6806d099c1a7d93c335d06988081d70fdc4c6e5250087f0fe1ee1e4fc7c6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.27.1
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Aug 2024 21:31:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Aug 2024 21:31:12 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Aug 2024 21:31:12 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 14 Aug 2024 21:31:12 GMT
ENV OTEL_VERSION=0.1.0
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-otel=${NGINX_VERSION}+${OTEL_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y nginx-module-otel             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile nginx-module-otel             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee57511b3c684acfe64e2025b557909406ca31f8dd53e0b0399a644c10ec1940`  
		Last Modified: Thu, 05 Sep 2024 12:39:08 GMT  
		Size: 38.5 MB (38513870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33791ce134bf8cde1f6f9473576cdbd3c087aec33541fa492051bc2dbb6872ba`  
		Last Modified: Thu, 05 Sep 2024 12:39:07 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc4f24efc205f5b338585fde826ee60f4d21fe7b9e95073e0676378a84140e22`  
		Last Modified: Thu, 05 Sep 2024 12:39:07 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cad04a21c991089f34f9da43b355f48785352cee1b72182a0d9ffcad16e63d9`  
		Last Modified: Thu, 05 Sep 2024 12:39:07 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:486c5264d3ad516a7daceee96f00c0999acc47c3c2230491df3f1071e3df93c3`  
		Last Modified: Thu, 05 Sep 2024 12:39:08 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3fd15a82525302ad66ab4a6c8109db464206085e4755cd0b7de443dcf5bb295`  
		Last Modified: Thu, 05 Sep 2024 12:39:08 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce799aeaa8524cdc894826c5909993891402456814c467cb7c8f3c20d687440`  
		Last Modified: Thu, 05 Sep 2024 20:56:49 GMT  
		Size: 2.8 MB (2845155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-otel` - unknown; unknown

```console
$ docker pull nginx@sha256:058d37965b9f9f3988af150b79acae5e7fe1a628aa1a82adfca7a780e256f4d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2973058 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f06494de8ef8dbaa85d104f18563bb7822d2fbd8cd56b1ceb9ec3de5cd1d7b1`

```dockerfile
```

-	Layers:
	-	`sha256:d71d7c783e3af266c75a67329e66038128a8911fba5a5c95d243d66c59e2551c`  
		Last Modified: Thu, 05 Sep 2024 20:56:49 GMT  
		Size: 3.0 MB (2951683 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f98b12a74388566573a16d1a28d544d8f62f6f502c73c2a645b10e6f0df6ef2`  
		Last Modified: Thu, 05 Sep 2024 20:56:48 GMT  
		Size: 21.4 KB (21375 bytes)  
		MIME: application/vnd.in-toto+json
