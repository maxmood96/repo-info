## `nginx:mainline`

```console
$ docker pull nginx@sha256:6784fb0834aa7dbbe12e3d7471e69c290df3e6ba810dc38b34ae33d3c1c05f7d
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

### `nginx:mainline` - linux; amd64

```console
$ docker pull nginx@sha256:fafd5f55296511cd0f1c991efa0cb85f323449bf643f3b6d760c6542f020d6e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72385735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e5f3c5b981a9f91ca91cf13ce87c2eedfc7a083f4f279552084dd08fc477512`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b00567da96412a0298328fad6b96aadd3bc9ca97e6683534da152b0b9e8a977`  
		Last Modified: Tue, 10 Jun 2025 23:28:55 GMT  
		Size: 44.2 MB (44151007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b81cfa547d78176e719c9cd387e35fbd95ce6e8500efb26d9fbcbac4dbc4f6`  
		Last Modified: Tue, 10 Jun 2025 23:28:53 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1bc5dc8b475d9de62c94cf69a139df17aaf7fe7bac76b5133d8048a058fb3c3b`  
		Last Modified: Tue, 10 Jun 2025 23:28:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:979e6233a40af9a51ee2c9894bd42ebf78a79c87cbed70cc6a3840a0952f3d57`  
		Last Modified: Tue, 10 Jun 2025 23:28:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2a7ba8dbfee4f222961ad1449648ab46a6cea044e4cfb374450325ecee8f67f`  
		Last Modified: Tue, 10 Jun 2025 23:28:54 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32e44235e1d55a34be577baa12271f067c0bf79ba4e1ca4e6ec484424540132a`  
		Last Modified: Tue, 10 Jun 2025 23:28:54 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:e3cd88cafe07d9dd9ca698e8c6770339833becbce9d7f4e68b78fb41c7290f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3140486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be60d379b6951f8b8f74f88fbe6bd5f2c5be65b0b47ce5187603bdae92db92d0`

```dockerfile
```

-	Layers:
	-	`sha256:46c98da933959a17a06c6f82bd1bd6365740600fb0352f6ab8bf6fb3c20eb456`  
		Last Modified: Wed, 11 Jun 2025 02:50:48 GMT  
		Size: 3.1 MB (3105884 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c117e190f2b5a90939bbb54f5d29061d26fa6efa7492fe156754517b1b831a4e`  
		Last Modified: Wed, 11 Jun 2025 02:50:49 GMT  
		Size: 34.6 KB (34602 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v5

```console
$ docker pull nginx@sha256:6dc08a9d8ed62c0899d1406e851727cad3ce7cf13aa946f6def77730325d273a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62449779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f36f175e87d6c752602218be107829548b97df2a2002fd36078751cb0a7e60a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:750907abe8bb5d66304ed40261e1579b6575871f6848cfbd720888c20afd3b67`  
		Last Modified: Tue, 10 Jun 2025 22:47:31 GMT  
		Size: 25.8 MB (25762396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6392e2e5840ca8a55db87c9e5f320d62f566277b5ea9b193c059ad4575f9d59`  
		Last Modified: Wed, 11 Jun 2025 00:09:07 GMT  
		Size: 36.7 MB (36682780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79c169f8ec55c154fcb6d5d854c79da43e6ef58114869ca846f5ae1952cf8029`  
		Last Modified: Wed, 11 Jun 2025 00:09:04 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7c62f5b066c0d08cba0cd931142518eab0ea48863397752e2686a15f1ffae3f`  
		Last Modified: Wed, 11 Jun 2025 00:09:04 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ff1bb99cedd78ffadfffce8877294e4f0cde03e7a155b5ab12cb8b10752968e`  
		Last Modified: Wed, 11 Jun 2025 00:09:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d14804382215f4defbc36d8ca41f5f6c77c295ad43b8fd771289db246b57a609`  
		Last Modified: Wed, 11 Jun 2025 00:09:05 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:631be5cabad884a3404da0e34a89c73df9b2fbf8c6abe70c948547e39b3e2d77`  
		Last Modified: Wed, 11 Jun 2025 00:09:05 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:14d270d21aee97e3437c4a3f8ff8a971b3a0f84f87293e09f9f23d3fa5994895
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3164653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebf1046ec5b0d6a993a39a320e76cd9f7155d159f4e020fc6f1e70cfafb7900c`

```dockerfile
```

-	Layers:
	-	`sha256:24ee85297177a4ec761a41deeda8706fa9e9a74989f959b48d8aff72d8aafc87`  
		Last Modified: Wed, 11 Jun 2025 02:50:54 GMT  
		Size: 3.1 MB (3129928 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86ae445fd2b6a4f1d2f24e623a19ee5bd245caf30bf62c74903926eb0128d26`  
		Last Modified: Wed, 11 Jun 2025 02:50:55 GMT  
		Size: 34.7 KB (34725 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v7

```console
$ docker pull nginx@sha256:ee5d7cac6f3353e0d19fb011d62d827c982b9a52aefac04976b8cc4ccb879f18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60839639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22abae52a82fa61e8751c5a41dfb9c8205d488d7ed22b64dafb242a472cd9a8f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6aafc35ac588733109bc0c55587676a69c7a13b7c2d7306cdb389c2db1299c9c`  
		Last Modified: Tue, 10 Jun 2025 23:58:28 GMT  
		Size: 23.9 MB (23938744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02f07a849a8a4c219a9b428a5b5d2a209b4ba8ce9698dc1acb8e33b7bb811b26`  
		Last Modified: Wed, 11 Jun 2025 02:53:41 GMT  
		Size: 36.9 MB (36896292 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40f14f9d7b0dafa0351565c5394174e3391c66150ded073f1ca0301081a4bdd1`  
		Last Modified: Tue, 10 Jun 2025 23:53:42 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8c35dcf16bd813380d5068226c3ff336b3309ae50ba2e1ae4c5d4324747a44`  
		Last Modified: Tue, 10 Jun 2025 23:53:45 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb5f9ce32d0e8bf47bc7b846891540379a5212a83a8f54d198eeb5a81b0a7a1e`  
		Last Modified: Tue, 10 Jun 2025 23:53:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd397f85dec06bfaebff4d84580ea01a542f01876a1dec8438e78bab10b9a8f7`  
		Last Modified: Tue, 10 Jun 2025 23:53:51 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e009f369cd24c95af2cd7c5711d04340ad55d40fb1ae298f87e73871027d2eb`  
		Last Modified: Tue, 10 Jun 2025 23:53:54 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:dc76e1be1d3f71c6cd1ab71f63f4c2bdcd57a1a3d8766b4305142ef54bdbdf52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3163313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:280b925fc76b53182f9ecaa26747f7539f93ec1b0686beca295bdb855d1946ae`

```dockerfile
```

-	Layers:
	-	`sha256:9e8de044310f9e24941e0e2c3082226b6743177b51258940762ce90a220b4f81`  
		Last Modified: Wed, 11 Jun 2025 02:51:04 GMT  
		Size: 3.1 MB (3128587 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8086650b2f6be77e6775bc9a04555f3cf31382962b14aab99a58fde5bb992c4`  
		Last Modified: Wed, 11 Jun 2025 02:51:05 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:e6017bb25206300fa159619f19498e0d682d0b48eed71fbdb08064b29888b103
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68836550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7791402a0bf5691936db0f42d40032ac6fb8441867416053f3ea06199de3e7e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06cdcf65323db36c0c23967e162e6d5ec2020a1b3c381f35e7ece68bd5aa24f5`  
		Last Modified: Wed, 11 Jun 2025 01:28:16 GMT  
		Size: 40.8 MB (40754280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27fe6a09bce876aa274da39977974372c2b0f48e8d84e7f64378890855a45752`  
		Last Modified: Wed, 11 Jun 2025 00:33:19 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca26eebd8366a11c538a54a50951724293c15c5151aaa4c0ceb7d3626678e53a`  
		Last Modified: Wed, 11 Jun 2025 00:33:23 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d29d0ca23f3e9c29b2988ee4aadbe8353f55e11403db8183bb445be96e956ed`  
		Last Modified: Wed, 11 Jun 2025 00:33:26 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447b5a3f15c69d32c90ed3b22fca996b7022fd9e5c240659404ca4053742cf12`  
		Last Modified: Wed, 11 Jun 2025 00:33:29 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71eccce642b8d6bb3266c66d1320b5810fa4109cd97e3f3ffe8a423deed7a546`  
		Last Modified: Wed, 11 Jun 2025 00:33:32 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:d0825145bf4d3eb9d429ca6828b5ed03bddee8e960bb4ff339868a68ed2f5d00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3141113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f53160950ce034067b7d16829d0f4d4784af5aa3db1b39b1dfe8d74515805f3`

```dockerfile
```

-	Layers:
	-	`sha256:80b78793f7d41d0136f3c30aa89075d2aac39846dd9380e8abe32811c0343494`  
		Last Modified: Wed, 11 Jun 2025 02:51:09 GMT  
		Size: 3.1 MB (3106335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4a87b30f7f7b83df50acfca07890233be10283650aef6ee6b31f1f18dfa97362`  
		Last Modified: Wed, 11 Jun 2025 02:51:10 GMT  
		Size: 34.8 KB (34778 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; 386

```console
$ docker pull nginx@sha256:2c1ee2371c776670cebad7f4fee298ed8979fdfc18d2c1bc49f17c35754259f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70752364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4fc1b1d076e3ec1b41c758c6b9c0f4b18c71df3c5a2923937739b932c045f2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:058a3aeb89e28180ddbe63deadf1eeb6d025dc8628edb3053932c82f4014ed50`  
		Last Modified: Tue, 10 Jun 2025 23:33:33 GMT  
		Size: 41.5 MB (41535325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff490355ee7c902ef816a5ff4875be7641c21b17cf3aba419bd18f61b59f1fec`  
		Last Modified: Tue, 10 Jun 2025 23:33:27 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2246ffefc86ba4746c6af208868df640736b771c06651879016b360bd985d7c`  
		Last Modified: Tue, 10 Jun 2025 23:33:28 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a0c8349b2aa921aa0e3faf609d0a8caa0f0a72de3f55a487985583211635c00`  
		Last Modified: Tue, 10 Jun 2025 23:33:28 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b13a1c84a0243c4450199b296217e43036e45dd187086a65f4e0ba169c984751`  
		Last Modified: Tue, 10 Jun 2025 23:33:28 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24614574c9847062a87a8ac0c0bc34edabd7c594bfbc24c6d961f4bac340b439`  
		Last Modified: Tue, 10 Jun 2025 23:33:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:f7f935273ac271a41b14c1a8d1b917cf7274d54b2c3828179a39a37a573f06f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3156295 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b9d8bb5f0bfa93a6226490277e12cc67f10682c3886b296909f45a13366c0af`

```dockerfile
```

-	Layers:
	-	`sha256:bcba204d4169b7c4463e5810cf1fc2f4fd3fb2c7df624b5ffcea3d58691a11a8`  
		Last Modified: Wed, 11 Jun 2025 02:51:20 GMT  
		Size: 3.1 MB (3121755 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eaf14ecaa949f4acc6befa0f7f07afe90aa95b0ab4f5d8f3f9cfd34e601e0765`  
		Last Modified: Wed, 11 Jun 2025 02:51:21 GMT  
		Size: 34.5 KB (34540 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; mips64le

```console
$ docker pull nginx@sha256:6c8dff1ca002b67bb2392d8bc33e9760f51cc2d3fa63236d1a82208c70e6d96e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68463646 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0323c28a9b3c77dd54deb2827cde1c88824c1e8bb2895f867fd06c86ee626204`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ac3f61581c7f5755d8598b3a0857c417db0251b17c0e4e4f43a5fc0e24023524`  
		Last Modified: Tue, 10 Jun 2025 22:48:26 GMT  
		Size: 28.5 MB (28516717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb01944c399fe31563bb197402aa211cd68e8b0440f6ea3a53196cdc85527cef`  
		Last Modified: Wed, 11 Jun 2025 00:52:54 GMT  
		Size: 39.9 MB (39942324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32a2ee1d3e420799fb2d07bba67b8e33b86c7853c5b11a981fd5bb101c08724d`  
		Last Modified: Wed, 11 Jun 2025 01:02:37 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f61d5402665573f89c79b2c550d02ee383b79c4eb7b67e5571005d963bdefc6`  
		Last Modified: Wed, 11 Jun 2025 01:02:41 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:851ff7c7bf2d57c423b2726b3887f57a696fb431c187974add0ce10acc978575`  
		Last Modified: Wed, 11 Jun 2025 01:02:44 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cdd9957df03d31e4edfaec4c8597a02805ee907b356d6494ef13d2ba7fb808`  
		Last Modified: Wed, 11 Jun 2025 01:02:46 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78be6ca24ada12b3d3df21e2031b7862ff8de79a4d4b2d4c44592de7c0dee817`  
		Last Modified: Wed, 11 Jun 2025 01:02:50 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:b7112e1503da38fc6625d14e69fe40ae3c4b96cc048b7f63258109032f1c6b44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1275ebcca2d76035720eb678a6cc455c579030d560ea618319f25efc0ad2f435`

```dockerfile
```

-	Layers:
	-	`sha256:3340ac7fb7e03dc1f813ccd3162037864c2440462e2c6d1060d8cf8dbb202293`  
		Last Modified: Wed, 11 Jun 2025 02:51:25 GMT  
		Size: 34.5 KB (34507 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; ppc64le

```console
$ docker pull nginx@sha256:2b224f2786060b77e5d5cc376b98dbb6cf062353c77828bf426ca1eab526b714
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77112565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc81be3b925e835fe6c24be4efaff506862d39e76424d8fb64dd2c11eb5e9507`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9cd5d5c131a8141631d87d9507a82e0549a2144689442301c07d2da80f39d19`  
		Last Modified: Tue, 10 Jun 2025 23:58:45 GMT  
		Size: 32.1 MB (32072795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e6ee8943c8a2f7ffe97bb97e4c473bf93870f675d08f2e6d03398a1f9c4f424`  
		Last Modified: Wed, 11 Jun 2025 03:00:28 GMT  
		Size: 45.0 MB (45035172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e68751d2773a1741a2e7808e44806150556dd93d15b435f2b8f192dc28100fb1`  
		Last Modified: Tue, 10 Jun 2025 23:57:50 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877ce7fba1603947aa7d68c1ffbf545a08193965cf88284daba227a1240102b0`  
		Last Modified: Tue, 10 Jun 2025 23:57:50 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e83c7ff51e602ae552955fce409e7b55f9f865ba61d37a0270834ac52014df`  
		Last Modified: Tue, 10 Jun 2025 23:57:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c22f82884e7e0d57e1d0cfb83a24aa320d0082ba0583216966c7198033a110d`  
		Last Modified: Tue, 10 Jun 2025 23:57:50 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f60d92c2778b1c49890b8f160fa61817fa9c9d2a67b4ace1178dabb3dcfd01`  
		Last Modified: Tue, 10 Jun 2025 23:57:50 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:c1c20d1dc1645062ceacf7c5ab5a02215f0a60b2c3b555f017b588ee14d6a8dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3171338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520edc9687679e0688c0e801e0f8432a4fb44fd7cf2369c0864baca053f397f2`

```dockerfile
```

-	Layers:
	-	`sha256:995e380390d3f849381ed064705990ff11f7d40861daf290a674d5c59a63efcb`  
		Last Modified: Wed, 11 Jun 2025 02:51:33 GMT  
		Size: 3.1 MB (3136656 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:270c1b10dd9e54068764239fbb70e7e49c4b8dd0ae56c64ae0de83df54664f50`  
		Last Modified: Wed, 11 Jun 2025 02:51:34 GMT  
		Size: 34.7 KB (34682 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; s390x

```console
$ docker pull nginx@sha256:89525ec29fd002ada8f7981d7a8aad5bed01a651b78b6d1a3b3228616d2d7432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67079716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0899c631059f89de2c7fafb693c0413d69789284d269ad8bdc12984a5d9e7f6a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 16 Apr 2025 14:50:31 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1749513600'
# Wed, 16 Apr 2025 14:50:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NGINX_VERSION=1.27.5
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_VERSION=0.8.10
# Wed, 16 Apr 2025 14:50:31 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 16 Apr 2025 14:50:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="c773d98b567bd585c17f55702bf3e4c7d82b676bfbde395270e90a704dca3c758dfe0380b3f01770542b4fd9bed1f1149af4ce28bfc54a27a96df6b700ac1745 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 16 Apr 2025 14:50:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 16 Apr 2025 14:50:31 GMT
EXPOSE map[80/tcp:{}]
# Wed, 16 Apr 2025 14:50:31 GMT
STOPSIGNAL SIGQUIT
# Wed, 16 Apr 2025 14:50:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0f8692aee2900a8d946bd57522757b4d5de83b6af52eb0aa55e05d787a077615`  
		Last Modified: Tue, 10 Jun 2025 23:56:06 GMT  
		Size: 26.9 MB (26887853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a88154f49851195b418fa0b91c754bead191e8ce7f22195fbde029a291c312cb`  
		Last Modified: Wed, 11 Jun 2025 02:54:13 GMT  
		Size: 40.2 MB (40187265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd39a7b0cf1fd561f315acab8cc64c29c041cef8e7e0d1050fc5b278aa743188`  
		Last Modified: Wed, 11 Jun 2025 00:10:02 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a944856ceedeadc5fa54cdcdfc93b19e35af83439573cc9b682d4964a9ca940f`  
		Last Modified: Wed, 11 Jun 2025 00:10:05 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e47a9e6400cfcb8ab1fb200f44c496eeed80ec50f4b204dddff057dc51e8afb8`  
		Last Modified: Wed, 11 Jun 2025 00:10:09 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a840fe3a24e981de7ec7793b6509bee0bbeda642e92ec95c365fbae466f3c402`  
		Last Modified: Wed, 11 Jun 2025 00:10:14 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57e860e976a5a9b7a8605250ff8d3f89ea0107707e5d786f23459dd5e2d9e759`  
		Last Modified: Wed, 11 Jun 2025 00:10:20 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:6e05297f9f1642d52fe23d86291a17c2ad2f63b5ca0e57c9313244fec9f2d3ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3151210 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d5ae0a591d4d573ec03564ee85527563622f0dd720dc8ff6de63d47fbc2281`

```dockerfile
```

-	Layers:
	-	`sha256:f51fbdac222e9f12b7af38b2c46dfd65f2d25e58d67d7c05889586ca77ba3a5b`  
		Last Modified: Wed, 11 Jun 2025 02:51:44 GMT  
		Size: 3.1 MB (3116608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c154777755563827ae735f6e9fd777292e85bf3aa79cd48f20ef536452e5f6ab`  
		Last Modified: Wed, 11 Jun 2025 02:51:45 GMT  
		Size: 34.6 KB (34602 bytes)  
		MIME: application/vnd.in-toto+json
