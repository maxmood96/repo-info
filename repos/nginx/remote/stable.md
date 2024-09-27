## `nginx:stable`

```console
$ docker pull nginx@sha256:d2691ab019a8277af26ff577cd36545626d780391aef1c1b6c906fb7002ebc9c
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
$ docker pull nginx@sha256:2aadacfb0a1a02b7101f5a46e72d6c46351c6c159f8b4adb1fb85435c1c5abab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71007585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ebdd2db239fe67ea1cc7d618e7d7bba7816de19bb50a6eeb1a14823ed6c5a4f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
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
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2285a31517ce5f8b1bcd31aa850b7f4c5580dd30d7509a77ad6511aa2bf19b5`  
		Last Modified: Fri, 27 Sep 2024 06:02:14 GMT  
		Size: 41.9 MB (41876726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72584ba57ec36ec2e7e245a0ae783b5b86277fc92f80bb52a05ae6003fffd7bb`  
		Last Modified: Fri, 27 Sep 2024 06:02:13 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cced715622945cba517b521cc8be94cace10185d008828d310f4d111ac82d4d`  
		Last Modified: Fri, 27 Sep 2024 06:02:13 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8e99cafdeadb1ece91fd481387b2e41ef3699140ec6b30586cb9cde7b39bec3`  
		Last Modified: Fri, 27 Sep 2024 06:02:13 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a90562b1f36719764e17d32f64b39b15c53423c7991365acf9def368ebebc470`  
		Last Modified: Fri, 27 Sep 2024 06:02:14 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa064a8f7f95bcb98bda1da51df8dcea81ba73a50e557db0317d8f002d7c456d`  
		Last Modified: Fri, 27 Sep 2024 06:02:14 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:7c150cf906d454e1f8d98b47b9e8180f9118c347b920337b3b3941a869a51edc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eed5dc14f5b47d512b7c9150a6cce52feffd115b69063b286c7577b66c1891be`

```dockerfile
```

-	Layers:
	-	`sha256:12ef1ca14ca8b22ee57c1d1df5707c9675bea24405e263c1bdb0e957191b6b4f`  
		Last Modified: Fri, 27 Sep 2024 06:02:13 GMT  
		Size: 2.9 MB (2940687 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1e054c29ccd1ffdcd8fa5c40d282923c99761984c4802bd4a1b2f65ce0b6205a`  
		Last Modified: Fri, 27 Sep 2024 06:02:13 GMT  
		Size: 29.4 KB (29438 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v5

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
		Last Modified: Tue, 13 Aug 2024 11:02:00 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

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

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:9a1d62fc4c433ccb8726c961f6bc8177e4ea7e85097497f69db66b1b9fd6a6c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830185 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f46807e36fbab9034cbe58c4a90be35203f4df70608d275df827d0f07d4ae3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
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
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0e6fb5c34cf5e9c9212ba07b7b1956d4e32f57d8434e7e5f978693e4facdf89`  
		Last Modified: Fri, 27 Sep 2024 11:16:46 GMT  
		Size: 35.1 MB (35107447 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5297f2db7121d24c40c9612e48899692bf8e51e8c8aca8d6d0b94c179ea9e71f`  
		Last Modified: Fri, 27 Sep 2024 11:16:44 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca5fd169b66ee0e35d3a72b0193b1b6a1c575fc5970f4446b8244dade9aecfd`  
		Last Modified: Fri, 27 Sep 2024 11:16:44 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f97edb5a99eeb195a8fe34cf87e3d7a5cef7fece877b6e11677996a1b65e2799`  
		Last Modified: Fri, 27 Sep 2024 11:16:44 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1fb129af4bf1c569a59aec42cb041c3d057a77aa3179ea278a630f7b911eb0a`  
		Last Modified: Fri, 27 Sep 2024 11:16:45 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389a672abf5ca4a3a0a3461f20b00df0af4d156c09980655537608f42e75c25`  
		Last Modified: Fri, 27 Sep 2024 11:16:45 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:775dc36e438422f04f6c8a39fff2395dbe9e0a7e0692099c9c120028468f59b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63e8525e0fcb428382271e68d31cd6df0a66550c49bb653afd82b1c8dbf14658`

```dockerfile
```

-	Layers:
	-	`sha256:c1462b298299a4f5e2020f6ece33c3b264a821a583434c58ab9cfbd40f6f7db2`  
		Last Modified: Fri, 27 Sep 2024 11:16:44 GMT  
		Size: 3.0 MB (2960676 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a1bff10f593f68baf599b38354dafa354054cf3131bdceff22345cec62c6b25`  
		Last Modified: Fri, 27 Sep 2024 11:16:44 GMT  
		Size: 29.5 KB (29524 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:0e1785cc00f5efa1c05cbffed44b88df36689a611dec123bd3c6ebebd2bfb169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.7 MB (67673034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f54f66f995855943802b9f875104327460a71ca1a3e31f6e9b5da90452a195ce`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
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
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60177a842d80fa7b1a1c01a474181ee516cdbdbef9c9f380f75fed3853929221`  
		Last Modified: Fri, 27 Sep 2024 15:32:55 GMT  
		Size: 38.5 MB (38512085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9cc6d2155851d9b2c7ff002c39ebf7ccc4ebb045be30ecb6cde5bd34e281c51`  
		Last Modified: Fri, 27 Sep 2024 15:32:54 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b764080c971218c1f22f1ee49d85cfc7a5b2f1159cd21ecd15a8692a416d0a7`  
		Last Modified: Fri, 27 Sep 2024 15:32:54 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc109a52c1e9a32996bb60ccc799a874985d581a7f075d06346a9cf643252add`  
		Last Modified: Fri, 27 Sep 2024 15:32:54 GMT  
		Size: 392.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61ea53676b82788a6c105332a94caab5bf5bf2c994331c6ffdb841f9b9f5750`  
		Last Modified: Fri, 27 Sep 2024 15:32:55 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f9976ba075b687b7c8c1f14c790691f1598b55d87fcce12dc8842d43686b658`  
		Last Modified: Fri, 27 Sep 2024 15:32:55 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:c6dfd4a0b2a806b4ad87ec7ac3c49b78d127c0f9b7f1445a28e20dc2f4624ac5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2970860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee9bedb6c4363e86bd3e2d6a5ea93b846c8b66733cf8c9e8ff7cec1c968217cf`

```dockerfile
```

-	Layers:
	-	`sha256:4e32abf56ac0467517b9aacc1673ba65176bcf50f8fd0f380062dc1f92aaf5d0`  
		Last Modified: Fri, 27 Sep 2024 15:32:54 GMT  
		Size: 2.9 MB (2941089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e32b00902874585d22a6f459768ab8fb573ca2fb1f2127d27c99ebb1e178e278`  
		Last Modified: Fri, 27 Sep 2024 15:32:54 GMT  
		Size: 29.8 KB (29771 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:340ac1d4d89eedb80bb500d65e139a4e048283daed9c080b520658622cf66ffd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69188848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9002f34bebb19661245e1c1ebc9bb00fe58342955c15084d9989264877eef37`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
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
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:483768fe99c8a59b9983eebdf9d440275dfb62c15175a2ed5f642485732727c6`  
		Last Modified: Fri, 27 Sep 2024 09:08:48 GMT  
		Size: 39.0 MB (39040039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74f23130534eefd455dbe91f2d7ee0588e55153ce6fd4d77610ae7b3e4b2933e`  
		Last Modified: Fri, 27 Sep 2024 09:08:47 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddcb5b7e97950841fd6bb83ae5cdac504571055083937b85720dc5fb560e2cc5`  
		Last Modified: Fri, 27 Sep 2024 09:08:47 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1ad0288dce343f360b499b8b9ad555b79cea9e1a5ec6189091ad8ca1d073320`  
		Last Modified: Fri, 27 Sep 2024 09:08:47 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4803672eac33ea5c959babaf49cd42de0ab01c3332fd1f4a0f20751a460edd47`  
		Last Modified: Fri, 27 Sep 2024 09:08:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d96b0f1975b16b38e89c87f1d0e125d242d3fece80637ce4b81e757040ac25`  
		Last Modified: Fri, 27 Sep 2024 09:08:48 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:e55b40d8eb9e97e20dd19e32fae9ed761c2e1f10e84fc385212ab658a7e2c800
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2983279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c3fd36f336606a184219575da6eeb8441426747971dd69cbdafb443efcd3629`

```dockerfile
```

-	Layers:
	-	`sha256:f46bfe45297e588b248b2ba82a72da407632cd20ea41ab1aa39f7d2302816476`  
		Last Modified: Fri, 27 Sep 2024 09:08:47 GMT  
		Size: 3.0 MB (2953881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ecbf0a6a6b4971af8faf2c3cf069615fb33056a93d05d9a2e090d07d966641d`  
		Last Modified: Fri, 27 Sep 2024 09:08:47 GMT  
		Size: 29.4 KB (29398 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; mips64le

```console
$ docker pull nginx@sha256:00594625b31376c34cdd167d7987527822ab814224400a7ffb931386ad21fa66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66692539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02a637b41feb868dfad415681bceb35903142c3a1177d8582a56030679d95732`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:9ffa4d53a074e91efecf5e26e3b67077f46165e0d042c1e6cf1b93c531ed2bc4 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
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
	-	`sha256:89502a0eae32ab684bc9df3d9922ee2874839b178a693286c4b866f5ca8e93f3`  
		Last Modified: Wed, 04 Sep 2024 22:24:11 GMT  
		Size: 29.1 MB (29125054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ea9a098ad4480bf68e827d472523090139fbeea3c7545b9bf512d6b139920f3`  
		Last Modified: Thu, 05 Sep 2024 12:00:12 GMT  
		Size: 37.6 MB (37562879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b513d2b24008cf4cd224b91ed5ca9fd72fdb1d3d73a3e07baceacb7045eec442`  
		Last Modified: Thu, 15 Aug 2024 18:39:07 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06a13ea197ba83cd7d961186da6a8838d0639c7926959ad28aa155573e9f8fb6`  
		Last Modified: Thu, 05 Sep 2024 12:00:08 GMT  
		Size: 961.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8babb6bd1f5ecb92fa747c08ddf396b67c6a8f0652a0f1592474d6d49e8c6f46`  
		Last Modified: Thu, 05 Sep 2024 12:00:08 GMT  
		Size: 398.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce04c687f15e35a87acec58156c5d82d9f927dab3e85bfbff9eb1d2a5ce6924a`  
		Last Modified: Thu, 05 Sep 2024 12:00:09 GMT  
		Size: 1.2 KB (1216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5afd3a4923b016c123c9c9836e93cf6bf6e2c71b7859071436aff309ca30afb`  
		Last Modified: Thu, 05 Sep 2024 12:00:09 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:18839c407ec4b1c62e17c1cf1671d893e8f4b4c3c744943f2c49cea4cd4dc079
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **29.3 KB (29294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a8efb27bdde65e5ba3b9f8e308e28c067a42ea99e731ab8cf40bf85c5f55eac`

```dockerfile
```

-	Layers:
	-	`sha256:576fcb6eb6f5c450e1395eaab908bebea96a55cf29fe74467b3b067012384038`  
		Last Modified: Thu, 05 Sep 2024 12:00:08 GMT  
		Size: 29.3 KB (29294 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:130671615b1d9a5b8665431173a63adf21bdbac65b46236f199c9034a4a16597
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75478188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c27d5f6943e18805070d4029f96f0c2dbf62927032bb4d3aaccb4ab744d52f3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:d83b2f8d4d3fd22a390140e3bebefb48e5f086d072ad6062f6446b4fc42ec7a8 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
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
	-	`sha256:f19b11698292330b7d980ed50b0141417eec298d865e0c1b305ce7a8b80b572d`  
		Last Modified: Wed, 04 Sep 2024 22:30:11 GMT  
		Size: 33.1 MB (33122358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f88bd507a7ea692b6ff2f80db5646c5247211c30d559302902f4d75b290acd3`  
		Last Modified: Thu, 05 Sep 2024 00:55:27 GMT  
		Size: 42.4 MB (42351245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aae69d9082e892078fc2db9b430094410d00903164234f60e4426dce6a077bcb`  
		Last Modified: Thu, 05 Sep 2024 00:55:25 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d74c7786d0b0c5747800d9b9a5c89490a080a0a3f6b89a626aa6b122da99bce4`  
		Last Modified: Thu, 05 Sep 2024 00:55:25 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d65de20dbee5917c8ddd42d078b25400d4f1dc10fa5bc1f2df6c720abd43528b`  
		Last Modified: Thu, 05 Sep 2024 00:55:25 GMT  
		Size: 394.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9aeabeeb30d1c17af8a6e98a6251fd5ee50e002e36338c4e4aa65138385c5460`  
		Last Modified: Thu, 05 Sep 2024 00:55:26 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2009cf6dff753d4151ff64e8fe98bc1b1d8c26981b1aafe55633bcd1c4ed2ffa`  
		Last Modified: Thu, 05 Sep 2024 00:55:26 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:a47241bb8a97babbf415512366c9d6b3a4a807361625f499850f392c35d43fc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2997655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb97eb2c9a23a9f5c458d926b2d180f5df3db190ff05acf65444dfa8f302ca20`

```dockerfile
```

-	Layers:
	-	`sha256:01e919318bc9da800e6b4ca963f8ac66e3f578d318ea99e89eb34210c00b26e8`  
		Last Modified: Thu, 05 Sep 2024 00:55:26 GMT  
		Size: 3.0 MB (2968167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8809d56b1058225745ddb94387c96023eaa8f07a1ef7d8814ec14d32682a9e39`  
		Last Modified: Thu, 05 Sep 2024 00:55:25 GMT  
		Size: 29.5 KB (29488 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:9368cf8ed60754fe61cc462d16b938772828a4a0c770c9488bb0e07f3c1f3f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.3 MB (65302942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce2dce7e5a80d5ee79c0d4ea49b260cc08451ab3952935f5ae2a86f2ffb5306`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Wed, 14 Aug 2024 21:31:12 GMT
CMD ["bash"]
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
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53a0c81023c48326a0073d912c3938eafa350f41cc962d17ceb5923a8f816f5d`  
		Last Modified: Fri, 27 Sep 2024 13:18:07 GMT  
		Size: 37.8 MB (37808330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cb8a3777211d439e1d7519779040560b530c4321076f0de8fae6aadf44758e3`  
		Last Modified: Fri, 27 Sep 2024 13:18:06 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db99991d2d576ab126a5218b62bd3287ebd89fe431365d0112b5bc9d0d7a3cf6`  
		Last Modified: Fri, 27 Sep 2024 13:18:06 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df6ab8218e94f61ad62c37c1824f01af710f5bffb32b6c22174a5d8e87d8c8c1`  
		Last Modified: Fri, 27 Sep 2024 13:18:06 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95076465f97a61a73fb9a42aaa40a07212356714244769ad933a725c0e074f96`  
		Last Modified: Fri, 27 Sep 2024 13:18:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23f10a7b7e961c0c19a5294df53ef3849035452aa92ef36e168d7a39d1441b27`  
		Last Modified: Fri, 27 Sep 2024 13:18:07 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:884fce576604046f7d9b7211b19aee014cbe22dbe8d6d3050d449a00d12910b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2981580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d528fdc63d52578153430358609e511ef257c069fb61949dd25fa48b08c356a7`

```dockerfile
```

-	Layers:
	-	`sha256:c3322213c0140e1c806b304b57141a32bb453baa04185d49690adc9161bd1af5`  
		Last Modified: Fri, 27 Sep 2024 13:18:06 GMT  
		Size: 3.0 MB (2952142 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:365d43f6a2fcb3fbd677fa0bb8ad42eb6665f77e527a9e93f5a422e76df3e44e`  
		Last Modified: Fri, 27 Sep 2024 13:18:06 GMT  
		Size: 29.4 KB (29438 bytes)  
		MIME: application/vnd.in-toto+json
