## `nginx:stable-bookworm`

```console
$ docker pull nginx@sha256:df6f3c8e3fb6161cc5e85c8db042c8e62cfb7948fc4d6fddfad32741c3e2520d
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

### `nginx:stable-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:680547a4d2c5d286012289e4a7def7f8269029cca67da04b4bdacd88fc92890d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70112102 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ef6eaebfc53650f3a4609edbf9d35e866f56b2c5e01d32d93439031b300f0b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7182e7b8bb70d8460a764c18ee3737352c5731163b517ec434cdac61160c7139`  
		Last Modified: Tue, 24 Dec 2024 22:18:05 GMT  
		Size: 41.9 MB (41875931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54ce070d3ce1607001222a1e6a2bc89c5a0b00a91ef78772ad99c331956e909`  
		Last Modified: Tue, 24 Dec 2024 22:18:04 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5cc0a5fd30d66a73160e630410bf38ac352353c377704d76fb119b7be79433f`  
		Last Modified: Tue, 24 Dec 2024 22:18:04 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:954f71c94ccf268d30dca4d1e374ba77c9bbd1613fd4e65ac7401a24582592d3`  
		Last Modified: Tue, 07 Jan 2025 22:54:59 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b90f21a19b0aec6d5bdbe4eacd165d70950211bc6eaba32a91e6cba9b56d920`  
		Last Modified: Tue, 24 Dec 2024 22:18:05 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7f0ecbff4459961a9504dea504fb31e972af4e851bbdf4f19d3e9329756ec2f`  
		Last Modified: Tue, 24 Dec 2024 22:18:05 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:503f9670f73e575040a2104b59f6ab6b3cfccd4014c995272bd336568bd49db2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2984474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a273847ae602ab8bc3e9180913ac1d02a6dd983c028f2119b8d576ccd0e48b34`

```dockerfile
```

-	Layers:
	-	`sha256:a6043df539d938934deb6f8947a76295ccdcbc2ef40e8613072fbed53ae4d09a`  
		Last Modified: Tue, 24 Dec 2024 22:18:04 GMT  
		Size: 3.0 MB (2954848 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6548a4c25c13a04dee4a71cf74d59560035c6f263f722a868f97c4cf9c6fde27`  
		Last Modified: Tue, 24 Dec 2024 22:18:04 GMT  
		Size: 29.6 KB (29626 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:b15e944113563088a22785544ddaad2cf67fb46d4da30709df6bd66d955a7ee2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63486953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13714b85a8dc9a5d029871b7cea97a1967f1865c7e1ed45a8570af72ca933151`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 21 Jun 2024 02:12:35 GMT
ADD file:0a38a76ef88f0bc858f9663f2ec636121970b50fcd7a62192be7a7eba71bd6b4 in / 
# Fri, 21 Jun 2024 02:12:35 GMT
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
	-	`sha256:1bc90b37f777aded897944b0ce596c103432c1b84f7b626b9fd4a53356f006da`  
		Last Modified: Tue, 13 Aug 2024 00:58:27 GMT  
		Size: 26.9 MB (26887303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fdeeb7deb642a66ac72d2e020b34dcc9a883cda95123e6eaa152addff963ed9`  
		Last Modified: Tue, 13 Aug 2024 11:02:01 GMT  
		Size: 36.6 MB (36595055 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f0f7a0251d012c18627543fbc3b6fd64a982e4249962c055ca56eb3e5262e`  
		Last Modified: Tue, 13 Aug 2024 11:01:59 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:425d7b047859764be40f088df50781c8c62add96b3cb1ddd58e73428efb5096d`  
		Last Modified: Tue, 13 Aug 2024 11:01:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63536dae477d2b3b57b5bc01b760efdd48f7303e75ca00760f54242365b9d13f`  
		Last Modified: Tue, 13 Aug 2024 11:01:59 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5db9142c81b73082e65165f9af6b7d1cd3d03cfb2081901cef0e638f00e63e6f`  
		Last Modified: Tue, 13 Aug 2024 11:02:00 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f3ea4c6d72d26d6438eeb2d5f9278b4a776894fc50b287b03bbd851fb179f3`  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:d3bb73dd2f64051b27a826def8047cc27f2b69ea4a7e043e27acd90e896a9112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c24e3d37c73cff991820608bb494603177c17bbce567289e13bb943aa990610`

```dockerfile
```

-	Layers:
	-	`sha256:02f36737802c2a5464d7c836c9fac13a7229ea2c080379127208457b0a86976c`  
		Last Modified: Tue, 13 Aug 2024 11:02:00 GMT  
		Size: 3.0 MB (2961518 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eddcbf7bfd4571c97aa6c0f7711a2103a957f6ca16550fc79a98e6b849b05b29`  
		Last Modified: Tue, 13 Aug 2024 11:01:59 GMT  
		Size: 29.4 KB (29433 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:c57541b1aadaff6ad50753cd3a90b5f9636831a76e7059b248c5a56e4859832c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.0 MB (59046283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b25c322df8c6eaf0c1cef17a33b531873473032f653b29092f455a210e300a75`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1734912000'
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:24f0da30a772db626789cda3e7b0911098d07574c40b30be943d43dec3ed685f`  
		Last Modified: Tue, 24 Dec 2024 21:33:51 GMT  
		Size: 23.9 MB (23933522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ce47dc9908d2b1cd1fe652a9fdc46812fbf3c925509ec3b04cf231ab45228d4`  
		Last Modified: Tue, 24 Dec 2024 22:42:12 GMT  
		Size: 35.1 MB (35108166 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf1305ebecb86f2ddab5588348cb50a7d893951ca9e61557428d00f1b2b6b21f`  
		Last Modified: Tue, 24 Dec 2024 22:42:10 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff8ab77f180889cd387e4e29e55236929ee1bda57dd9813b03d4f4debd4d8145`  
		Last Modified: Tue, 24 Dec 2024 22:42:10 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a399b232361524bad38e1b1a3745501a29a0793fc8309a00f55f274710470f65`  
		Last Modified: Tue, 24 Dec 2024 22:42:11 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ec6fdb4f8b2e81f8679d4eabd2f2ce70bf03a057d54ca21be8eeefef298871`  
		Last Modified: Tue, 24 Dec 2024 22:42:11 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b29116e1203e692028666ddde67a66642b5b39501907f41d555dcd922a128f2`  
		Last Modified: Tue, 24 Dec 2024 22:42:11 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:81dfcf0a7a10079cdc9c6225cccee69239a18d4b4ead0ce10a6b1a72485c10b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3004724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0fd5336e4019ba07ef4930256bf30caf0ad5d4c3da3bae0c1f8d47ec1d4429`

```dockerfile
```

-	Layers:
	-	`sha256:c01838a0b778e718afccee98b2b439ba303f67ff30c81f1c660dc8b0c105fcf1`  
		Size: 3.0 MB (2975006 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be3cbfb4d6300e1a581b9254c7a52334e3f047f80cd0b400daa6329d63b71469`  
		Last Modified: Tue, 24 Dec 2024 22:42:10 GMT  
		Size: 29.7 KB (29718 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:ddbef5f031931a9b7ff72b58b6d907d93593ae5556ebc1c7f38d1753616a4649
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66576377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a86cd5b7fd4c45b8b60dbcc26c955515e3a36347f806d2b7092c4908f54e0a55`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 07 Jan 2025 21:57:10 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989308e5efbd7389c6d543de10f3a291c65008025099eea002ca704da784089c`  
		Last Modified: Tue, 24 Dec 2024 23:03:37 GMT  
		Size: 38.5 MB (38513064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef3dd9169685fa276a8a62c4c8a1b21c7fb6c378cbc10e0b6af51f3f367aa9d2`  
		Last Modified: Tue, 24 Dec 2024 23:03:36 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca859205549e87184aef14b13fe324de3b9bcb4fa86ab89c95ac55f05ae10709`  
		Last Modified: Tue, 24 Dec 2024 23:03:36 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd7d65b627bfe6b420fe78245cd8f5e5290a5a242f57ad5bdad1606628fe442d`  
		Last Modified: Tue, 07 Jan 2025 22:53:39 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:906d56a624a1e7826c366d1e07e344dad3f2c4dcf05c74cfb33b0e1c6400f89c`  
		Last Modified: Tue, 24 Dec 2024 23:03:37 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b98a4d439f6c0bddf32694826d25b895f97cc636d808db2225eb4d37fe938e`  
		Last Modified: Tue, 24 Dec 2024 23:03:37 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:453555e265830875a2f17d292025b8c2db227809627607b5d4584c1982b90cdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2985005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74b455af70506ceb66bfe0273732159ac53a6d06f5d09e4a05f05a43f9d1a8f9`

```dockerfile
```

-	Layers:
	-	`sha256:e3811a5eb0bfb9893d353feb3cd90b88f24705b64eb78d5ac172365c0eb0b399`  
		Size: 3.0 MB (2955251 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b869acb8a857914ce30d0b0b0809ca43573a633b904c0c39917a4b9d3c5a6f5c`  
		Last Modified: Tue, 24 Dec 2024 23:03:36 GMT  
		Size: 29.8 KB (29754 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:c3967cafba9eb65cc5ad9864f641731550dbd6afd44d9798820e777476df3492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68249930 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31739131b0acc38dd5a02f77eab76eca8e06cfa5d379cfecb59821ec7888a0b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaac5469ab6ba679883551252355f23dd887a89de7713829e995bc6490fad2b`  
		Last Modified: Tue, 24 Dec 2024 22:18:08 GMT  
		Size: 39.0 MB (39039955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ac0d463806957aac36ae4c6baee2cf9c7f31feec9e7c06efa8bf4666ea68f64`  
		Last Modified: Tue, 24 Dec 2024 22:18:07 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6565414b1e1036345a9eb8946251beb67b5810b55d89d7ac8706d94da81d0e2`  
		Last Modified: Tue, 24 Dec 2024 22:18:07 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a23e85816cf163085264f67d72a03358f64f199d0ccf8eb46f5c1113d51b9027`  
		Last Modified: Tue, 24 Dec 2024 22:18:07 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:408994e60c3d9c4e26431acfaffe4970ab483e4b14ad0122794ffda82dd3fa3f`  
		Last Modified: Tue, 24 Dec 2024 22:18:07 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a4ad8489aa1b8865a44f9191ee42a9621bac9674c7c95b87e4324d9b6d1e2f`  
		Last Modified: Tue, 24 Dec 2024 22:18:07 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:0e53c15b53e62f51d4f758a54980db1651ec96c1281b68ba155478b18d973a1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2997723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:feaca145fadae0feedfad3e68daccc282c67dde5e2ec6c34fa8ae92ff55499a0`

```dockerfile
```

-	Layers:
	-	`sha256:ea644088dbfb550f990f89f5d8724db9aa851e5b16582d9360c32e2fe26e1705`  
		Last Modified: Tue, 24 Dec 2024 22:18:07 GMT  
		Size: 3.0 MB (2968139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27139130ff031c7d2329561eb1d046d65a6ada7282587e303db9fa66cd4f08a6`  
		Last Modified: Tue, 24 Dec 2024 22:18:07 GMT  
		Size: 29.6 KB (29584 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:15b616ae92a214eebb5f5a2baaebcdacaa7fd077e9466f18862d4fcf3d18a0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66072751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4ab5e1327b74e10ef1bda4532ec1327fe70f48904632c8f000980929ca971a0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1734912000'
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:8a9f899eb883b68bbb36209214842bc927b7c446aa0471f0b241ae7e76adb6e5`  
		Last Modified: Tue, 24 Dec 2024 21:33:38 GMT  
		Size: 28.5 MB (28505873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7be3136f0ab7781b2b6a45c51ee24ae894cb726cb08a372c9a220598c1c6a4e`  
		Size: 37.6 MB (37562282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24a7ae8d0aa3ee13c3dc8a6cea58edf191304821946de39a9382ee82935d8f02`  
		Last Modified: Wed, 25 Dec 2024 00:02:48 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d84b3a1e65b289a4dd067d176349e210b2bde587f33d186197ad9500caed0946`  
		Last Modified: Wed, 25 Dec 2024 00:02:48 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6ef1b83747eb36c172d7e2ecb01c1deda3589e3d87f87d822e6c01d3aef179d`  
		Last Modified: Wed, 25 Dec 2024 00:02:48 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de6cf5398955fd4d8e28973aa782a305fa17876428e16705b115c67cf2660fa8`  
		Last Modified: Wed, 25 Dec 2024 00:02:49 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d82bd32ef6f198bcb59dca41af407216ddaaa6d108cdf74a016d7c9b79ea007`  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:56d66559b37bc4238bbfe72ebf5294ee5e001f12e6964d617958dc5e102ad5c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.5 KB (29495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95a0a168ca66ea8d981a49a9452b405c4921634440f704af2788e82de3ab41e7`

```dockerfile
```

-	Layers:
	-	`sha256:6539b2ecce85725e50ab43353b097f046414e5c41fae77b3294ed1f855a73bd2`  
		Last Modified: Wed, 25 Dec 2024 00:02:48 GMT  
		Size: 29.5 KB (29495 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:42cd8bd50b1f1dc9a4dad524e320952cc2625f7e5a1c1eec1a836bad0864fdcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74419980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44e9f0750de531a7f179cefff548914b473902ac61a217aae4e5d40244a1d29f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1734912000'
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:4a1ea4d3c9e0863e99d27aae6dac9a4b908a6413e758c7785d8fefe555b0e760`  
		Size: 32.1 MB (32063240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c10aae66b6d9a805c1ac7b166fba9ce4be7db3ee84bdec36fd5dd4194f6c31f`  
		Last Modified: Wed, 25 Dec 2024 04:30:59 GMT  
		Size: 42.4 MB (42352148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1ab99d95a8bf3a4af9d76068b1fbce19edec7174fbebac6207e9715cfa451ef`  
		Last Modified: Wed, 25 Dec 2024 04:30:58 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c350627c5e9e75a92b6d7d64d1aa722e726da07a950f5ec18d4485663fee440`  
		Last Modified: Wed, 25 Dec 2024 04:30:58 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cab87c88d64ff1d9c19ff283f8fcb8e0d62967e231a02bcf3b3a73d041dc573b`  
		Last Modified: Wed, 25 Dec 2024 04:30:58 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52a0910601d8d64f5c8cc957f551d2f4ad5ba524ea6e66a7e693abc2fad4a21d`  
		Last Modified: Wed, 25 Dec 2024 04:30:59 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a8adbd23d63b8228d696f63e9ea6a77dfd4987bb8db6fca3247c0b25a9ba0af`  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:a85cf2648c747b3113fd66ae1ee010a83ba458e6ac1a7506162e0ab99636e2dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59afec9e2c3fb7e11cb6745c40f80f5e4ce586522c7660264acada89ee3bebd6`

```dockerfile
```

-	Layers:
	-	`sha256:fa670766c9d5f8254a65773778991b93a02bb083ef727020cbc54ac0246b126d`  
		Last Modified: Wed, 25 Dec 2024 04:30:58 GMT  
		Size: 3.0 MB (2982605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a15a095fa3a79fd808f1e1d1a9b990e3300c45517815ac16ed1a13b68c87f96c`  
		Last Modified: Wed, 25 Dec 2024 04:30:58 GMT  
		Size: 29.7 KB (29681 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:d5523634e51a2efff697a477aff4e00b3a7dea792c7c104c714c684b81955e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64694801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c79efdc644baee5927c26ea8ae1d9a4f0b74a952ef04a9b12088c025be187db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1734912000'
# Wed, 14 Aug 2024 21:31:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NGINX_VERSION=1.26.2
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_VERSION=0.8.5
# Wed, 14 Aug 2024 21:31:12 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
ENV DYNPKG_RELEASE=2~bookworm
# Wed, 14 Aug 2024 21:31:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
```

-	Layers:
	-	`sha256:0e7e84bd4cca9e29f08dfac96d436e65bdd31929520e73147137b382fbc89b70`  
		Last Modified: Tue, 24 Dec 2024 21:33:49 GMT  
		Size: 26.9 MB (26878901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60fdf2ea8a5a8ec73e219291de127281c5469667618fb40c92a3d00e4cb932c`  
		Last Modified: Tue, 24 Dec 2024 22:45:21 GMT  
		Size: 37.8 MB (37811313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7495334faccd1c74d8691b6ae51fd7837faf660a89ba628f6bde59f307483f65`  
		Last Modified: Tue, 24 Dec 2024 22:45:21 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:389f741faf5dd17152a4a0757dc3b0dec653d246f49e54877fd33828b669856f`  
		Last Modified: Tue, 24 Dec 2024 22:45:21 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bb9d66d6dff4c75d615d132ef9ef3cc05da6a6540d90da38416ff5f92ff28fe`  
		Last Modified: Tue, 24 Dec 2024 22:45:21 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4be83b78be37bd2b6b7976f0f90a347946a03c6665a4a68b745775c2400f9b32`  
		Last Modified: Tue, 24 Dec 2024 22:45:22 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:affbad1fca2e1f7f1f36f86441a3fc200fdece080f7ea26f3c6adc003033fb25`  
		Last Modified: Tue, 24 Dec 2024 22:45:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:6c6098cf0afd77f88d275a92e41bb017da4e21994267c09c9c1f953a43053640
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2995867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3311883b3660299178c45fa48895983592c7a8f41ab7090a7ae34f73fd4d4909`

```dockerfile
```

-	Layers:
	-	`sha256:6db8fbcad291d2ff5cb345caa89ffa4b1603921e4c688865f557c0179db42d87`  
		Last Modified: Tue, 24 Dec 2024 22:45:21 GMT  
		Size: 3.0 MB (2966241 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4ad84fb3b21fce32eef17e2a55525772495533aca3c1738047d6d902c5ea555`  
		Last Modified: Tue, 24 Dec 2024 22:45:21 GMT  
		Size: 29.6 KB (29626 bytes)  
		MIME: application/vnd.in-toto+json
