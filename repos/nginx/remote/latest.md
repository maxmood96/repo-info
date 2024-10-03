## `nginx:latest`

```console
$ docker pull nginx@sha256:d82f4a1b74aa1d6289584f70267f8c936809cfdfe96b2de28d3998e879dbb240
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

### `nginx:latest` - linux; amd64

```console
$ docker pull nginx@sha256:10b61fc3d8262c8bf44c89aef3d81202ce12b8cba12fff2e32ca5978a2d88c2b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71007604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9527c0f683c3b2f0465019f9f5456f01a0fc0d4d274466831b9910a21d0302cd`
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
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd986b3703ae056a0ba06e883b07848db7a08681864a2ca96849670230d25b2b`  
		Last Modified: Fri, 27 Sep 2024 06:02:11 GMT  
		Size: 41.9 MB (41876744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a52cbc3961ba3b2d424f040554938ea89e8094f629441405348a9030d89999`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1875670ac8aafd9b7a00cdaa081e296955ed186616d04f4974c9cedaa21b331`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af17adb1bdcc43b1306f84a35848fe299f204328a28a1d307b4219edb02cd888`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97182578e5ec1388c464990f781f56a4264379cfa3a621f15fb28831c848cd63`  
		Last Modified: Fri, 27 Sep 2024 06:02:11 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67b9310357e1d8cc6aa835063af4579da53d6322e777a9890418b12c7b2d9080`  
		Last Modified: Fri, 27 Sep 2024 06:02:11 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:241ebc260ea2ad427576f5e2f9ad1d01ce03e85ead0bd9204519519113399c13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2972560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28ef0a50edf49b22201c40be7e1bd3263065a2aca6e37fec1f9a9cf20b2a05b6`

```dockerfile
```

-	Layers:
	-	`sha256:c52ac1ed6cd1b5b2ff6eced0a228a4228732d6606b6261da0c9e0a3920e2eacb`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 2.9 MB (2941881 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3961546ca4aba8162c4e2ff7114c2237f0a6dff0fc38b5de12f3b01e4353178c`  
		Last Modified: Fri, 27 Sep 2024 06:02:10 GMT  
		Size: 30.7 KB (30679 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm variant v5

```console
$ docker pull nginx@sha256:6289301f3b918b98577fe0f80c13761aae5791b0059ed9e1d554edeae7c54b82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63486853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b0fe21fa62a85adf6fa39d8cfef5f362ba5228ff75005aa2c5a9c1e0d72b491`
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
ENV NGINX_VERSION=1.27.0
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_VERSION=0.8.4
# Fri, 21 Jun 2024 02:12:35 GMT
ENV NJS_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
ENV PKG_RELEASE=2~bookworm
# Fri, 21 Jun 2024 02:12:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             echo "deb-src [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list                         && tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get build-dep -y $nginxPackages             && (                 cd "$tempDir"                 && DEB_BUILD_OPTIONS="nocheck parallel=$(nproc)"                     apt-get source --compile $nginxPackages             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
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
	-	`sha256:98f3556f59b9f88eba944c179422b399d4d7bfee3378a29a8862546b31db50a7`  
		Last Modified: Tue, 13 Aug 2024 10:52:48 GMT  
		Size: 36.6 MB (36594953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92caa6f3caa0e0fe67d53d7b91e307527b520916b6426a223e759c83e9a578e5`  
		Last Modified: Tue, 13 Aug 2024 10:52:46 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e69509d0506dd0826ef57d4be729625e271094b2af13899b1f083f9b3fce40b`  
		Last Modified: Tue, 13 Aug 2024 10:52:46 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2793ee3d86e16f73853c4d1d4dea81336502052b0750fbda33583ba0c79728f`  
		Last Modified: Tue, 13 Aug 2024 10:52:47 GMT  
		Size: 396.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eac478447bda26a2c5c6d1376a2bbbe757a52cf44e5209718622824a37d88d4`  
		Last Modified: Tue, 13 Aug 2024 10:52:47 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f7dd557bb2412ed882ff952341ac5657512844e81cbb667a4a8dca90413f1d8`  
		Last Modified: Tue, 13 Aug 2024 10:52:47 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:3e576b43defa219d279961a042477c8df1b2e46d15ec8cd98827eae750e33fa6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2993450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cee8d328cf95e07e12cacc31b28e8bf2fd66b1d2fadf86aa1fe28ed647bebcb`

```dockerfile
```

-	Layers:
	-	`sha256:555f667f5397434da94069656e81eaae6417bd9e5a1344d2d64bb4bead76d372`  
		Last Modified: Tue, 13 Aug 2024 10:52:47 GMT  
		Size: 3.0 MB (2962744 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c697ba63a55a1b87c3ecc7ee3022d4952751931cb83a8d7a427452465137bcbe`  
		Last Modified: Tue, 13 Aug 2024 10:52:46 GMT  
		Size: 30.7 KB (30706 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm variant v7

```console
$ docker pull nginx@sha256:f24b660f892b023fff2fd0ab33f43bf5d115ccef8b9887e1812d3e622492e92b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.8 MB (59830547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfb3dbc4950d3d7238f8488b64d04b61ff66268d6eefa6c29246d31e3bd8b12f`
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
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eb5e1253d5a7272601b8a32b50f0a3e77be8785c7964df5d092151804e7f559`  
		Last Modified: Fri, 27 Sep 2024 11:12:19 GMT  
		Size: 35.1 MB (35107818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e93b4a07a0e0331b38386718484a232f34c12d37e1f37886f5cc9218febc2e94`  
		Last Modified: Fri, 27 Sep 2024 11:12:21 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:147e18a15d1025c8c8e674178ec0bcc043cf3ccdced44810d535330fc6e5d1f6`  
		Last Modified: Fri, 27 Sep 2024 11:12:18 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2111c8e4f5a984a35e892342377f14b0d7cd504eafee74a79eca8713002f5e9`  
		Last Modified: Fri, 27 Sep 2024 11:12:18 GMT  
		Size: 393.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cee0c8a02360af595c57dab3c17124123bb1e71c786e1b529d40076e9bd744bb`  
		Last Modified: Fri, 27 Sep 2024 11:12:21 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1a4e49272ad3b8b80d2ba0c3b00ca1ac4539728ee0c5056dacfa8318b1db6fe`  
		Last Modified: Fri, 27 Sep 2024 11:12:19 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:4bfd038babf896c3b3b3e68fd038f64f688915af21204f00d58a7f7755aa2f27
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992700 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93cf80d4a7e967f51c1d800e494289573744b4a940468d3b8382193667472064`

```dockerfile
```

-	Layers:
	-	`sha256:cb12b0e63eb3b12347079d72638e63195d63947a4cbfd390aab7806965af7db8`  
		Last Modified: Fri, 27 Sep 2024 11:12:18 GMT  
		Size: 3.0 MB (2961902 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6b6a163e68d2be458c1cd34395847c1bcff75b4fc9f770a1d8cf2439bfd5d64f`  
		Last Modified: Fri, 27 Sep 2024 11:12:17 GMT  
		Size: 30.8 KB (30798 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:96c43ba316370e0c1d1810b9693e647cc62a172a842d77888c299f3944922491
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69579083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:048e09038596626fc38392bfd1b77ac8d5a0d6d0183b513290307d4451bc44b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 27 Sep 2024 04:38:17 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Fri, 27 Sep 2024 04:38:18 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c62fa01086040cd1f46a1cca2e6d9757c0516e5076b0c47cb8f599f8047a920f`  
		Last Modified: Thu, 03 Oct 2024 01:12:48 GMT  
		Size: 40.4 MB (40418119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:783efa7200714b88d9642a0b17a3c1b100033df3b8873ec214b388360ec3c8f2`  
		Last Modified: Thu, 03 Oct 2024 01:12:46 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9346e20ffd27cbb75c776445a5d69b2624e840e40733b3b7e2f4ab2f2094287`  
		Last Modified: Thu, 03 Oct 2024 01:12:46 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0917afa5d8b7098a9044df4dbfa166c23ec293e703f132489146bbdc57083fc`  
		Last Modified: Thu, 03 Oct 2024 01:12:46 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e905ecdf6023bc5ecc0c08ad95b3b946340fd38938717e62c49a7df96d214dab`  
		Last Modified: Thu, 03 Oct 2024 01:12:47 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66b98279bfb92df7ae2c28fa75e830faa9a7226079ef916d7352d9a64ac35467`  
		Last Modified: Thu, 03 Oct 2024 01:12:47 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:74df3a8a3f68bda11bb5190b465cafcd31cd0df178b72da5f56dcc62b36274e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2976937 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a752f8ed5cb2e34ece302158918f48591fd88ce682e6046863189b37cc06b7`

```dockerfile
```

-	Layers:
	-	`sha256:850fa4e76ec9700e83086aaea19d82b3068086e1e7804f1ce547e9d9110b557b`  
		Last Modified: Thu, 03 Oct 2024 01:12:46 GMT  
		Size: 2.9 MB (2942331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a0d8f8c9211b23230ffad727eda3a09829e1ee7a6cf9b879e28fef6e70ea39e`  
		Last Modified: Thu, 03 Oct 2024 01:12:46 GMT  
		Size: 34.6 KB (34606 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; 386

```console
$ docker pull nginx@sha256:1608b077388621cb3973be539b1642956e47a6fb803818b5505cead3d69a50e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71318533 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7c391817b3cf0bb437b42ea963a9dc8a96519053ca21588b5ee3c51e2a1995`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 27 Sep 2024 07:23:00 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Fri, 27 Sep 2024 07:23:01 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7182128fef98152a0dc7bae2be8539c75c7e7af6980a5297a5c8ed65f29625d`  
		Last Modified: Thu, 03 Oct 2024 01:03:01 GMT  
		Size: 41.2 MB (41169720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05c91ba3be2d627056b95b3b608bf29b9756855c857d54399cb5093b80af8007`  
		Last Modified: Thu, 03 Oct 2024 01:03:00 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35a994176de3cb7ec934e79ee1723b798b194697ddd810a6cc2cfdcfa01825c`  
		Last Modified: Thu, 03 Oct 2024 01:03:00 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86bc3b1eb0a8c4652c83ee76395e4478b47669da29c120edacc85e82b5384b37`  
		Last Modified: Thu, 03 Oct 2024 01:03:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:226e90cc965bf6ca55ddd098400cfe587d9ac20c490db0c7200735b9e06ffc2d`  
		Last Modified: Thu, 03 Oct 2024 01:03:01 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4380a6936a30197b6d2a56829023de5b5f202691ab35be4b5f784649dc3cf9b7`  
		Last Modified: Thu, 03 Oct 2024 01:03:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:c22779972c1228817da828f82ef77a8d616cc5b17a026b48ed3ee9d4dc1c7f88
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2989432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732f698f77d33dcdc8c8aacfd587d35ce26d41622c1a5b2a1e8a8e114efe8099`

```dockerfile
```

-	Layers:
	-	`sha256:891e50925df94ed32be412935f08fa3724a15a3ce3771d147041bc69fe779c41`  
		Last Modified: Thu, 03 Oct 2024 01:03:00 GMT  
		Size: 3.0 MB (2955055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ba21e483d3b05b122a2f6449a835ba588f83f5d27ad0ab39afa3213134ccbc5`  
		Last Modified: Thu, 03 Oct 2024 01:03:00 GMT  
		Size: 34.4 KB (34377 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; mips64le

```console
$ docker pull nginx@sha256:6bd2a16b519edf6d841c1efe7816668f741e9144001f63cad821e527cc88b58f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66690441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46bba21572c4545288e4b959674a746b67ca841973364169cc3205ab628ee070`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 14 Aug 2024 21:31:12 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
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
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c43a1a64fea10bb0b290bbe90c3f420c7041b2922958eb29dbcbd7e8ba5260`  
		Last Modified: Fri, 27 Sep 2024 23:54:24 GMT  
		Size: 37.6 MB (37560991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f384dd91348a47639851d3567ef8d6a46bc4400a56099d3a38aad5a36b33abcf`  
		Last Modified: Fri, 27 Sep 2024 23:54:20 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea8fee9c8e57cb91382e6b5ba600dc6233fac9b2db1025216ba79bc80166c35b`  
		Last Modified: Fri, 27 Sep 2024 23:54:20 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc8cab10e53baaadd50c5cad4b11ff003da9cb95f4d9302f286700076ff7681c`  
		Last Modified: Fri, 27 Sep 2024 23:54:20 GMT  
		Size: 395.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12922108f325769dd35b09595eaa95e7d5674436d6f3c67a915bc5950fbfe589`  
		Last Modified: Fri, 27 Sep 2024 23:54:21 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18fc164aaf7f197d3dbb2570db266fc3f3fe8414f11d1d3166fefb94a76cfa71`  
		Last Modified: Fri, 27 Sep 2024 23:54:21 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:4f53a37ef6c3f68a5227ca2f5a4eaea301c7ed639529a21b9916e1d708518d7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **30.6 KB (30572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8132eec08b1edb49f6a6badac1e7b68ca5f4418bfda851ffb0edc7fb40ac1b98`

```dockerfile
```

-	Layers:
	-	`sha256:f938ccb5d8428fa0977750997fd14e82cc72ba8ee841a9263b2259a6844b8d72`  
		Last Modified: Fri, 27 Sep 2024 23:54:20 GMT  
		Size: 30.6 KB (30572 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; ppc64le

```console
$ docker pull nginx@sha256:5d944fb59cfbdff8211fba43275ee319538366222ca4733bfce054d1ab29daec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.8 MB (77777095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1d8c113a30a9401db59a175d2bfab0487ba63a4c1eea51ff5a483fdcdf1b3a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 27 Sep 2024 05:33:07 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Fri, 27 Sep 2024 05:33:08 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3b7577ea770d19a53f4652d8d8d9df9f5e26b833baaa7caaf31a85446dce6d0`  
		Last Modified: Thu, 03 Oct 2024 01:25:57 GMT  
		Size: 44.7 MB (44650328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21bc72ce7bcb165fd44d792298a11f1bdfd63dcf12d9d48cc159011e7a97921d`  
		Last Modified: Thu, 03 Oct 2024 01:25:55 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:197cbcf357b8d4d123cd5b8a380c09334b3aa52235f6e4a2f216ce444075aaa5`  
		Last Modified: Thu, 03 Oct 2024 01:25:55 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae83975b3f4351610864dc4f34c505d2cafd69d776fbb194393bced5f9772c9c`  
		Last Modified: Thu, 03 Oct 2024 01:25:55 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:139077b7d55064a843f23581c0aba8517405d757def29194664911c1e93bbb0d`  
		Last Modified: Thu, 03 Oct 2024 01:25:56 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a6fe5185ed9624baaab867970f1c3e5fd3263b3c8647c584086c769a2e79e23`  
		Last Modified: Thu, 03 Oct 2024 01:25:56 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:0cc9c5b918ba701d27c1756703ae936d1ad038bfca4b8a398898e436807a7b1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3003944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9237e7fefb1bc421d4d92ae4396f3db0478d537b9894d5bbf7fe0e94a39d42d0`

```dockerfile
```

-	Layers:
	-	`sha256:0812d39884d2a9abba4bb2cf923f50b780b1a60629f57c94dd7ec6fc27034cd5`  
		Last Modified: Thu, 03 Oct 2024 01:25:55 GMT  
		Size: 3.0 MB (2969434 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:efe24308e353786d433358178201bc1971a80115aa963bacf1b01e6071599e70`  
		Last Modified: Thu, 03 Oct 2024 01:25:55 GMT  
		Size: 34.5 KB (34510 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; s390x

```console
$ docker pull nginx@sha256:708aae7852141dc2a7c458701de9faf4c13d1d424fc993339f6b9b2d99f92b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.4 MB (67354264 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ecb6294e303714bdf1f0a8ed8f113a033b37efc2393e8d48c52aab1e997ae810`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Fri, 27 Sep 2024 02:43:25 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Fri, 27 Sep 2024 02:43:26 GMT
CMD ["bash"]
# Wed, 02 Oct 2024 17:55:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NGINX_VERSION=1.27.2
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_VERSION=0.8.6
# Wed, 02 Oct 2024 17:55:35 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 02 Oct 2024 17:55:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="6982e2df739645fc72db5bdf994032f799718230e7016e811d9d482e5cf41814c888660ca9a68814d5e99ab571e892ada3bd43166e720cbf04c7f85b6934772c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 02 Oct 2024 17:55:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 02 Oct 2024 17:55:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 02 Oct 2024 17:55:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 02 Oct 2024 17:55:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe43de9b44d34683c756aa29490fdb1d01eb4ffb91a47d74e2c210a996e14f69`  
		Last Modified: Thu, 03 Oct 2024 01:33:31 GMT  
		Size: 39.9 MB (39859636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49f81f5277309b5222d87f62cb33cda6024bc06c9e5f6b2ba72a5967d0063e61`  
		Last Modified: Thu, 03 Oct 2024 01:33:31 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a9a7bc8f08cdb516b81040c96aca29afd55834361b88841e9e4d5f248eecdd1`  
		Last Modified: Thu, 03 Oct 2024 01:33:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96ddcfc61aca8b7b036f36e93444bb4915042241139bf421c41742f1396bba28`  
		Last Modified: Thu, 03 Oct 2024 01:33:31 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:749738cdabeda40c526840f2d6fb7e95114b6e8487daae6e432ec54b7227470f`  
		Last Modified: Thu, 03 Oct 2024 01:33:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:182ec49671498eb85382553f27c86fdb33a1787ef490292d59707f968be05b2f`  
		Last Modified: Thu, 03 Oct 2024 01:33:32 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:4fde4fc7009a7de0900afd6f1e60571be30cf3933b7026434461a75f3fafbcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2987772 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60674e4b0550a935d22067044c64acfeeb79a7268bd25701dbd07a450ed9385f`

```dockerfile
```

-	Layers:
	-	`sha256:a5f842e83acf034b8ce146fe6a80fc1ad6528ba9270740e03c82fb080564218d`  
		Last Modified: Thu, 03 Oct 2024 01:33:31 GMT  
		Size: 3.0 MB (2953336 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5081b4bd05266e09f3f6d2f2071caac11ba151a27d3e0710e315b5d15b214f3`  
		Last Modified: Thu, 03 Oct 2024 01:33:30 GMT  
		Size: 34.4 KB (34436 bytes)  
		MIME: application/vnd.in-toto+json
