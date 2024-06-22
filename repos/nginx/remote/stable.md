## `nginx:stable`

```console
$ docker pull nginx@sha256:e43407ce353dfe317efe69eb33716e61d0ae613080ef7df65fb08e39bab36ab8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:stable` - linux; amd64

```console
$ docker pull nginx@sha256:0160662d5d3b5eddb9b3493c0e646c84105c67c0b7bcee3dbb82cdc0537c065d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70990059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1bda1bb6f7f0fd17a3ae397f26593ab0aa8e8b92e3e8a9903f99fdb26afea17`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 01:20:56 GMT
ADD file:5f9954090af042b377ea0d1d184faa64d2e9d4c946b6c3898d52aff47e764056 in / 
# Thu, 13 Jun 2024 01:20:56 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.26.1
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2cc3ae149d28a36d28d4eefbae70aaa14a0c9eab588c3790f7979f310b893c44`  
		Last Modified: Thu, 13 Jun 2024 01:25:30 GMT  
		Size: 29.2 MB (29150430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e53bb12304c65b6ba38fc31f583d53e0ff901ad4b50b39201004f51b40d3f7e4`  
		Last Modified: Fri, 21 Jun 2024 19:54:36 GMT  
		Size: 41.8 MB (41835027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aa01a1edab389e9d2e1a6d1d5a8c226b65e9bacd501df74a3934e03c56c537e7`  
		Last Modified: Fri, 21 Jun 2024 19:54:35 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:288dee00f66dd5091ad5b481a4485f4043f320e94621220f33ac7108f1aea0c4`  
		Last Modified: Fri, 21 Jun 2024 19:54:34 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce262edfdce5b59dbab524965dcc0a0121ab3aaa7f67b7aad8660a5f82b90b08`  
		Last Modified: Fri, 21 Jun 2024 19:54:35 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695e83fb6bbca8bbb8f5645f3614f7a4aefdd46c981b203f63def340b499a8ca`  
		Last Modified: Fri, 21 Jun 2024 19:54:35 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7bff473cc460f7b9487173df388cc4363d27daf0fb641a6e0edd861730e7959`  
		Last Modified: Fri, 21 Jun 2024 19:54:36 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:a54b2c6adafe8ae6ef2be35597239b557763328abd22823d2b68ee620c411866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2936624 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebc51ccc96dd19c007f18cd6f0881bd8caf2b5052f525fbaf7d816a2d0a8115a`

```dockerfile
```

-	Layers:
	-	`sha256:0a880c7db9480550fd684a34443751f211d58d5da56ebc5e5b2dee95aef6bf68`  
		Last Modified: Fri, 21 Jun 2024 19:54:35 GMT  
		Size: 2.9 MB (2907277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:45ee875ef3431b7643a7a43a0ae8e0ee568ea8c228fc2ac0468c7a26274767ed`  
		Last Modified: Fri, 21 Jun 2024 19:54:34 GMT  
		Size: 29.3 KB (29347 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:aad6e4d3d8b6e7f77101d41d3fa60087f199cef104fed6c03baf7fe1a8e83dd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63512230 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a2155b22ce6ac93f95508a4c8ab2a3c73b572b14c8d68252a2935a24a9de7b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:48:32 GMT
ADD file:9ca492786bcb3648d90c47fc2dba3c8239eea7a0689f6a17ee25a9f5129aabd5 in / 
# Thu, 13 Jun 2024 00:48:33 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.26.1
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d50583018de0ccbb239bef29dd375ae0ea018644d67a37b4fc29bec08b3b1a33`  
		Last Modified: Thu, 13 Jun 2024 00:51:38 GMT  
		Size: 26.9 MB (26909975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74836bc015322d97d77c8056933d1ffc7a3f9ab99ebd82a6fc2a3fb0566a9c0`  
		Last Modified: Fri, 21 Jun 2024 20:06:20 GMT  
		Size: 36.6 MB (36597643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ec15bd5168bc63769bd1c5e5f796ebaf36062755aa9d6a9123e13a2fc0e8c93`  
		Last Modified: Fri, 21 Jun 2024 20:06:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c44d18751e04ec3330cefc84f6e13c80019f64847732a5a958e8edc38462998a`  
		Last Modified: Fri, 21 Jun 2024 20:06:18 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3a4f110b75da46d48de6911274f73f3bbbe1dd47a699d17f079ea52d4d2a2e1`  
		Last Modified: Fri, 21 Jun 2024 20:06:19 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41b71a234d1b6e8d371ecaa224e601d2fce719a0936ae7d912e7396cd1c83df4`  
		Last Modified: Fri, 21 Jun 2024 20:06:19 GMT  
		Size: 1.2 KB (1217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55386dc3c58f3539716392f36c869c6fdc9ec5f28da15785eea4e1aa2f65e7b7`  
		Last Modified: Fri, 21 Jun 2024 20:06:20 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:fe53c7a162cfbbaf74c36fa8d53d9dc270c5d6edba0ccde96e69c541ac3b8d67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2957483 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f38781355c59fb77999239bccac6a903b4cff34be60dc7a5ddb075c3948f6fc`

```dockerfile
```

-	Layers:
	-	`sha256:ce4a975333a9100d4eb581a444da200c04d2df266957fb27a8dc7dfbc8308d02`  
		Last Modified: Fri, 21 Jun 2024 20:06:19 GMT  
		Size: 2.9 MB (2928050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b0c24829f21b1b1c9a30b4c70e561384b9359ea64313cc754f3618fffef018f`  
		Last Modified: Fri, 21 Jun 2024 20:06:18 GMT  
		Size: 29.4 KB (29433 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:5fba389a83e015fe6fc49c60e807a9252301382770a55a27681152535db99f01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59847201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c47211c0abe616a3331f7b40accc48691fe07465ac4208acc203be80f87fe221`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:57:41 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Thu, 13 Jun 2024 00:57:41 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.26.1
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9500439afa30c42972d4afcb63f3a1fa88c7e3e205470cfffa3a6286b8aaee7f`  
		Last Modified: Fri, 21 Jun 2024 20:06:27 GMT  
		Size: 35.1 MB (35102395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60ed272fe0e5927544af84b832a29b330d5e97a52ecc1e486a94a176c7dd4a7e`  
		Last Modified: Fri, 21 Jun 2024 20:06:26 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94b09661e432b5ea81c4a283472f2d51a79690e1bdc37d3187fdcf2241499875`  
		Last Modified: Fri, 21 Jun 2024 20:06:26 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85cf60f8870b74c10d7251b9735cb2b6ff0cfea6e9db343c54488024ff2753ab`  
		Last Modified: Fri, 21 Jun 2024 20:06:26 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcde0abdbb929367b78a94f7ef90f101582e586de4d8a434f758b43ee61bef4`  
		Last Modified: Fri, 21 Jun 2024 20:06:27 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10095877ee65d278e6077cc9e7210c31a6435dac73f19cc25e31d13e8e243140`  
		Last Modified: Fri, 21 Jun 2024 20:06:27 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:5d33fe87d377dc9cf82251c82b8e361e99d74a66e32a7522930ced31c9dd7073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2956699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f75f6aae74fdbe70960ebed7563b00be1a1750435ccd7965bb53c3279fd995cb`

```dockerfile
```

-	Layers:
	-	`sha256:6e6f59b25752499fbfb1083ccc3d5e9539b6eae790ffdda78c38f5e0d225a6d2`  
		Last Modified: Fri, 21 Jun 2024 20:06:26 GMT  
		Size: 2.9 MB (2927266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:290cb427e2b2c03bc87e45367241088d0782ca54265a24b5a4291937ccb2da6a`  
		Last Modified: Fri, 21 Jun 2024 20:06:26 GMT  
		Size: 29.4 KB (29433 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:97164499ae0739e0368717ffc7f1a0d725e2142d08d97772f3d55259fe289127
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67649750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d3caadc252cc3b24921aae8c484cb83879b0b39cb20bb8d23a3a54872427653`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:39:50 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Thu, 13 Jun 2024 00:39:51 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.26.1
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44bd577a0515d832ba54221558aea4d4f3445ca44903ea88bbafd5a589a83e8`  
		Last Modified: Fri, 21 Jun 2024 19:57:24 GMT  
		Size: 38.5 MB (38465483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:908af0e8c1d1610e8475032e1ed070b80017f7c07985d617e2598f51ddbd87e0`  
		Last Modified: Fri, 21 Jun 2024 19:57:22 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cffd9be3a7338a7864dd909afaaaa4e8e12dc0bbce035b0eb40273fbf96e3dd3`  
		Last Modified: Fri, 21 Jun 2024 19:57:22 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3d1eb6ff761947b31089d61ee9242ccdb34ac8e0b31da52958f7e38301581c`  
		Last Modified: Fri, 21 Jun 2024 19:57:22 GMT  
		Size: 397.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c84fa18c390584eb7448f1e9efdafaf6c3fedbe3acff8f95929b9adc1839e0af`  
		Last Modified: Fri, 21 Jun 2024 19:57:23 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a213c1a42c721dedf7d043e0cb34a97d19f2cfeedf556cec8ca0aa07f4d9e8b9`  
		Last Modified: Fri, 21 Jun 2024 19:57:23 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:2ad1c4fa1f14b1e62c2363cbf39538257376983ea53025f342256d820424543c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2937359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a24ae0a2c4efa6f27b9f4dab18d49c6faa19daf2ae8952f5a3933ed4d0cdfe71`

```dockerfile
```

-	Layers:
	-	`sha256:fc091335851af2eae142114986ad3e912887f589b3e8d47cc964420d55146963`  
		Last Modified: Fri, 21 Jun 2024 19:57:23 GMT  
		Size: 2.9 MB (2907679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54efe945b447fa4c5c0448722d83d965f3db7773c46dea131e65298604012763`  
		Last Modified: Fri, 21 Jun 2024 19:57:22 GMT  
		Size: 29.7 KB (29680 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:2cbbb9b88cf06e31c804b7b475275c8f23b6b5bb39b7b7e9f6fbab045f49374c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69143287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad199e0380008d05cb06a9f7e75585415bcc8139c8377c90fa794483d7f0fff`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:38:56 GMT
ADD file:d68e899424fb360eaf2a6f2f35e06dc87f5841c13cce853d3e0710f969583d10 in / 
# Thu, 13 Jun 2024 00:38:56 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.26.1
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7adb06274fdba91ff3ec0873bc068b9a785bd5e3ff48e6f1d9e855048f1f0a66`  
		Last Modified: Thu, 13 Jun 2024 00:43:23 GMT  
		Size: 30.2 MB (30162659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6799f69f12952470021ab375fee4fbcfc6897c2e9646cb96ceab24793d634737`  
		Last Modified: Fri, 21 Jun 2024 19:59:29 GMT  
		Size: 39.0 MB (38976026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b831e78d8e20641c11c527baff6e2c7bae6a43cc1ab4316a5532885d6461b1e7`  
		Last Modified: Fri, 21 Jun 2024 19:54:26 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d041779c36c61a409bebd64a5fc051fd42dfa505297be1201c92bd487f3b47e`  
		Last Modified: Fri, 21 Jun 2024 19:59:27 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6973b844c80661205b18897e1cd41c6d05cc0fbea63c5d24278189adb2d312c2`  
		Last Modified: Fri, 21 Jun 2024 19:59:28 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3869c438a364bda6307c07ce0b9f65bd5c12b4149d2dbb979a5e98395ce109ec`  
		Last Modified: Fri, 21 Jun 2024 19:59:28 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f10d52128ab44f7868f53749dd29719db108f56675fc709b6138dbc852d7a70`  
		Last Modified: Fri, 21 Jun 2024 19:59:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:8692abde63e90dd860b64ce717ef1fa70c2cc1f9ddf8178b2fa75b9059728a0e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2949779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5064c096c891e9d2decda0831f33835790fe2b79f055fbf1de2be08c96fda11`

```dockerfile
```

-	Layers:
	-	`sha256:a1d5224cd301ece672a6bc8c76d63d2ae9e4cdf0ff0068b5805fc71858ec1fbb`  
		Last Modified: Fri, 21 Jun 2024 19:59:28 GMT  
		Size: 2.9 MB (2920471 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:44ad4f8b53ea5a687c923d4a5e71b6543888c55d1c8383492a502c6571ded960`  
		Last Modified: Fri, 21 Jun 2024 19:59:28 GMT  
		Size: 29.3 KB (29308 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; mips64le

```console
$ docker pull nginx@sha256:9f4dea65a80fc455cc4a48dd2ffa215fe63f72dfdc34e8c696e1aad575f574be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66676305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67cca324b703cf2262b8f23dbb46b80f81632ee09b7f314de1db0ca59f5267d6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 01:10:34 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Thu, 13 Jun 2024 01:10:39 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.26.1
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cf8966b6f2a4daf570a7e32a0d834e2c4b830553e7a124fe91fbaba9dd0f450`  
		Last Modified: Fri, 21 Jun 2024 20:44:00 GMT  
		Size: 37.5 MB (37527881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2924d97e49ff48e9f441a1cf11c70b2302b1f8f7a262b14dfe9fd26bfc54ef35`  
		Last Modified: Fri, 21 Jun 2024 20:43:56 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13616ab4c18db97e669a533730120718ae4037bda18ceac405cfe30e67bb88f5`  
		Last Modified: Fri, 21 Jun 2024 20:43:56 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b615d9f2ff2464a0a1e3ac077e9ddd427f753b89735c00511d376f1f18dd99a2`  
		Last Modified: Fri, 21 Jun 2024 20:43:56 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a2622bb690b0c52467c2d75953a96ea0320bf5bb8c58dde4bfca668a09deb5`  
		Last Modified: Fri, 21 Jun 2024 20:43:57 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76474e204005fc7765bde4bb014346b0e9f3f4a2699b733b5a25e20cfa18b351`  
		Last Modified: Fri, 21 Jun 2024 20:43:57 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:de01aaf76bf99ee9ed4d65f1240e719a01314ddd913e48fed628e16cdbc0da1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.2 KB (29161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98a999077c0ce8aa837836fc0c8363fe6e884e2c3680366d35e52af1915d03a`

```dockerfile
```

-	Layers:
	-	`sha256:a70bbc477c0d8b7699da5317d659345c56518c81cec20d408e5350b83a874ad0`  
		Last Modified: Fri, 21 Jun 2024 20:43:56 GMT  
		Size: 29.2 KB (29161 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:6449e5130511671f4c483f81e45722828daec50a5f186625cdf25dd46a4ae952
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75432259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2131f8209307e670820c463ff6fde34e273ce3687da28a0d536204e69578f5e5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 01:17:04 GMT
ADD file:26d639147c70c8e3b876ab5c2950b7b7e7c654b878e69cf7a82a7cbdfdb31024 in / 
# Thu, 13 Jun 2024 01:17:06 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.26.1
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c4f33295caca163b437a6dc1ad770a1f2d84b4d5e78e832bbe0fb2f064aeccfd`  
		Last Modified: Thu, 13 Jun 2024 01:21:30 GMT  
		Size: 33.1 MB (33141195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ef73bb4350db94bbabb78b5cfa477108008ef5e160038104d93d387b8871c1`  
		Last Modified: Fri, 21 Jun 2024 20:09:47 GMT  
		Size: 42.3 MB (42286458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea5d57ba83534686087d6f50ebcbe6a2f76a14b4401ef11bafc968a09e2195a`  
		Last Modified: Fri, 21 Jun 2024 20:09:44 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ab59303e81d49dce13e1fcfc4f435b72a0fb67bdfbf7d3df792de332a3e866`  
		Last Modified: Fri, 21 Jun 2024 20:09:45 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8814058fb88fbfb528e9efa166e33f135edbe1df4b6713478b56f35bf2f1b278`  
		Last Modified: Fri, 21 Jun 2024 20:09:44 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8dddc3d2a52779b77eb567bd80409e18346387d890fc6f9bf316727f4a7d4308`  
		Last Modified: Fri, 21 Jun 2024 20:09:46 GMT  
		Size: 1.2 KB (1215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a8d291bb1beb111a6db6f668ff1b864ed6574380e9a1d8bc0dedbb227885027`  
		Last Modified: Fri, 21 Jun 2024 20:09:45 GMT  
		Size: 1.4 KB (1404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:b3b0c016930bf459b5c878fb466c0ed5f984853af48391cbef3a3af7b080465a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2963917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feab74df6acd2a60229b06029761bf243d1fdb3d5ae71d637321ff9c14e556ff`

```dockerfile
```

-	Layers:
	-	`sha256:616c209b0757c48e4ec05a3e1e9b58d7189557451ed477d10703bcb0cf83ece4`  
		Last Modified: Fri, 21 Jun 2024 20:09:45 GMT  
		Size: 2.9 MB (2934520 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2aad3a2426d324ac06118f0302d4562a3027a8131ca445c5680dbd9c7341be8f`  
		Last Modified: Fri, 21 Jun 2024 20:09:44 GMT  
		Size: 29.4 KB (29397 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:7dbd580d6308344646a9301b220f45521ae4fd772aaf1e17cdc3ebd0b94f8f14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65282721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af00a70b9679362551aaa54cb08d904ac8aeb4536dc6f7a6a83789cbe553253f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Thu, 13 Jun 2024 00:42:38 GMT
ADD file:e4d9e24430546fda3cf8c73efdaa45b6bf1014a23d4d3c0247fe341b3ee9212a in / 
# Thu, 13 Jun 2024 00:42:40 GMT
CMD ["bash"]
# Fri, 21 Jun 2024 02:12:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NGINX_VERSION=1.26.1
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 21 Jun 2024 02:12:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 21 Jun 2024 02:12:35 GMT
EXPOSE map[80/tcp:{}]
# Fri, 21 Jun 2024 02:12:35 GMT
STOPSIGNAL SIGQUIT
# Fri, 21 Jun 2024 02:12:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:06561002b4f942b877c60f94bd44315c2e0580cc0ae30f060660bdbcdae21d6e`  
		Last Modified: Thu, 13 Jun 2024 00:47:43 GMT  
		Size: 27.5 MB (27512459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e5576dbbaf3104f24fd624d9aa0015d1740f5ee5b3fd18f650829f33846236e`  
		Last Modified: Fri, 21 Jun 2024 20:04:25 GMT  
		Size: 37.8 MB (37765651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e63f8dc918b9f29bf00ed1a09929bdbd2788761edbbd4f52b522359a03ab274`  
		Last Modified: Fri, 21 Jun 2024 20:04:24 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70e6fd3739b505b75612b832daa630e0a2061960da3e5aa5af693063bf878805`  
		Last Modified: Fri, 21 Jun 2024 20:04:24 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eda08ea65fcb83aa1198c17ca78e76b601740fd40791ac92b57f57e3ed16c0e`  
		Last Modified: Fri, 21 Jun 2024 20:04:25 GMT  
		Size: 399.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:334973419d26374d760debddddb540773d4671c96be3edc1292d8cad82cef40b`  
		Last Modified: Fri, 21 Jun 2024 20:04:25 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dacb2a4b6b2d7db4a7411c50e2a1afeefaceb873a60b137c5233b0ed52798bd2`  
		Last Modified: Fri, 21 Jun 2024 20:04:25 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:281e09fbe76e1ba71d51591981ceab93b1ae6103aa9a64e9193f3197ecf7f9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2948365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47fd1b806aae9d5ffdbd332611f61dcaf3307b91644e47d61f6f10d4a551dda0`

```dockerfile
```

-	Layers:
	-	`sha256:33834879bcebc5fb0e6291cdd3917ae33fe58831b7307a82536f88ffb87935ec`  
		Last Modified: Fri, 21 Jun 2024 20:04:25 GMT  
		Size: 2.9 MB (2919018 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1b3f324e54968b0fb96b577a2f0b11b4d315f82de430bf1360169e4f8300c661`  
		Last Modified: Fri, 21 Jun 2024 20:04:24 GMT  
		Size: 29.3 KB (29347 bytes)  
		MIME: application/vnd.in-toto+json
