## `nginx:stable`

```console
$ docker pull nginx@sha256:eaa7e36decc3421fc04478c586dfea0d931cebe47d5bc0b15d758a32ba51126f
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
$ docker pull nginx@sha256:2db14d54fba7c2a618b209b48b8b0b798bf161df95d3e823ff6471c8686b51cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72380822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93ad19b5b847f64ffb1df64c55e6da69a9ea1c9c00af759cc5d1851adf649cad`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Tue, 03 Jun 2025 13:30:15 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b9ebf396424ad22bacb3d78369e96a6d887d96f258ffe41a5239a2ced66b824`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 44.2 MB (44150906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40d6655d5ba79f8ef6dc86e2f41b9f906094c90667ac10b1711d3babaa2d2578`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f3bad97f6025dc0a654aa02a5a3d1717f52103e6b79217dda2fd66bee15a607`  
		Last Modified: Tue, 03 Jun 2025 13:30:19 GMT  
		Size: 952.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:549226c4c0afc9c2812c7d6155e91ed7c5731405880f9e5b0602eb8636864844`  
		Last Modified: Tue, 03 Jun 2025 13:30:20 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cb882c6067f02340afb80ead6072955600a73baa9c0ca5fec4ea9173b181f94`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddd1dd60e7e59b64d78fe48f83410650a07dc7d159faeaf6efeb5d16f5ace049`  
		Last Modified: Tue, 03 Jun 2025 13:30:21 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:ec5131a6a6f1fc029c9872de5a68502a03662318e4b88ce784ff4c69c0418e9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab9390e980e5b55bd9d86aa8f3e839f3fa70618ac7a9a612177970f6d3e78d9f`

```dockerfile
```

-	Layers:
	-	`sha256:9293e5831d11af54e42311cb2a9de6491fbc0babfd1d806fcd1d41179c91f170`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 3.0 MB (2987922 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7bfb01979830729185c0c590dc6e62bf0299ae425cde7f15915f318aee167291`  
		Last Modified: Wed, 21 May 2025 23:12:55 GMT  
		Size: 33.4 KB (33381 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:b5ffa633e02dd9b243b9d66805d3afdc1456d0b8f8270fe8ce8ac86e4288fb87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62445525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:831228962abc6c648e0676a03678e88e2fca0ac5b8238f4724c213447d924511`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:fab452a77ecb21a2e30922ab3eed19310b6d56763bcfc4e4bd31f28d9747f745`  
		Last Modified: Tue, 03 Jun 2025 13:33:58 GMT  
		Size: 25.8 MB (25756898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4979ded8451cf352decf314a2a304fe1afcbca5c0823dafa3299bd90e54961e5`  
		Last Modified: Wed, 21 May 2025 23:57:27 GMT  
		Size: 36.7 MB (36684027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04481936b3f9bce9dc1f8ad6c9621ef737e2e6bc8af40dc62650d538f5776b49`  
		Last Modified: Wed, 21 May 2025 23:57:25 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebe457326890c0cb561181887a311da76ce7d44d0b8457a0f82ed159e4137e03`  
		Last Modified: Wed, 21 May 2025 23:57:25 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e40c02ff3b066d7087162e1fcf96e856e680bdf2789471b8cfdb00f87521b8cb`  
		Last Modified: Wed, 21 May 2025 23:57:26 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75929b6ef97eaa9fc84aae635ff2f252ef3c73efc89bf8dae0ef7c0f149f4399`  
		Last Modified: Wed, 21 May 2025 23:57:26 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ace239c5c5ca8b5efcc8c7434579002f5b713663da25ae74d456bc6310fb88ba`  
		Last Modified: Wed, 21 May 2025 23:57:26 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:88238bc7efe6bd43ad2c03dba7c0e0f3d85b9895cc6b5417efecaeaaaa66448e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3042781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef97249660fc9f98b292bee540bebd6fdcc61c5d660e27d1b614db6254bdba8`

```dockerfile
```

-	Layers:
	-	`sha256:0a044cb3bdfe3a4163db185f02dee62e8f527a88c4a2d567ab4a14daa6640f97`  
		Last Modified: Wed, 21 May 2025 23:57:26 GMT  
		Size: 3.0 MB (3009308 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e5ef5158bbf019737977f53167601070fc47057ea082a4088d35dea962a8e940`  
		Last Modified: Wed, 21 May 2025 23:57:25 GMT  
		Size: 33.5 KB (33473 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:5e79df284e13771fb090bb7cfb1adcc6312430a8f3fffce1ef186857ed8b34a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.8 MB (60834437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ab2ff1e0406575ddafe707173b164143132ca88f2fbd2797b63c596a24f358c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3726bc5cceb817ddfc7c2e1dbdfb4900fc6e27b680d63b8d751b06952753b6a1`  
		Last Modified: Tue, 03 Jun 2025 13:30:58 GMT  
		Size: 23.9 MB (23932922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:104d2a2bacdd7b323080e8366aa8713d6f1e8cf8cd7286ee0e0432051de6f6bc`  
		Last Modified: Thu, 22 May 2025 00:01:07 GMT  
		Size: 36.9 MB (36896909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8de37de14c6a9b901bca29d8311091e21e115aed6b63eb6e54f3c4289595ce3f`  
		Last Modified: Thu, 22 May 2025 00:01:06 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a4e3eb346748aefe0d88db6ef889bbc81b543528652717ba001efadecab83f9`  
		Last Modified: Thu, 22 May 2025 00:01:05 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14ffad120bf9f248f85e3d3e73e3acf93bbc8e6158b17a0a49ba15a4eda63e7b`  
		Last Modified: Thu, 22 May 2025 00:01:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f406a066bbe4cb116469b9f0398828f0f85b00f8ee6a8649e1c95601bf1fe764`  
		Last Modified: Thu, 22 May 2025 00:01:06 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:081bcc0ec8432e3ec1d032389233598bc72836f36ffaf4e2632be520f2a2c012`  
		Last Modified: Thu, 22 May 2025 00:01:07 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:e5b2ca108af6132775937e8431da8316685373954b66bed9f95746b29a97b688
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3041440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2c37c876de4da0a7b4a9ee06297bfba167710920e05a4ef7536709366ccf8c6`

```dockerfile
```

-	Layers:
	-	`sha256:c0b035551b963ac7a1db5c68954424a5dfefedd850ef2ed70f32aa416ba4f562`  
		Last Modified: Thu, 22 May 2025 00:01:06 GMT  
		Size: 3.0 MB (3007967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2578b76c080503907766e24565281f2ce2ef38fc4f1df8c648c7ea5b6233144a`  
		Last Modified: Thu, 22 May 2025 00:01:05 GMT  
		Size: 33.5 KB (33473 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:8a69403980d6d9ea8ca0bc81391b5a49e13876290188e1318903ef5db456ef06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68824934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d3b0302d5ce4b34284c1ff742e6005fec3467aaee928820904e6f304c1bdbf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3344b4d384131b49cde0abb048ec1693148980cee30619fb37f6c67ab19a700a`  
		Last Modified: Tue, 03 Jun 2025 13:35:30 GMT  
		Size: 40.8 MB (40755057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34234cc449f9de2a237fab2d55916dc3defa6b9509432cb3a6c930e35027c9d7`  
		Last Modified: Tue, 03 Jun 2025 13:31:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d248d3ff83244304e9c25a9bf00520267f4ad07cc05292f13d028a0594e1469`  
		Last Modified: Tue, 03 Jun 2025 13:31:19 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:567c9642f4dc8cee60cd32205cd245a489876e966aae2a24c3214a855001526a`  
		Last Modified: Tue, 03 Jun 2025 13:32:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9474da7c59e49f888d96017979bf63d1fe175a93132291ddbc0ee203bb52731e`  
		Last Modified: Tue, 03 Jun 2025 13:31:20 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98e8ecdbfeef2dfcb2743daf4dd748fcbe2a4559e05272d278ece378f3fa204b`  
		Last Modified: Tue, 03 Jun 2025 13:32:43 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:ccdd430dffaa3d452ca551424b51ca69868b1836ba843aaf162c03a72d175f90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3021834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:274b8b3cb922a73841dc03f4453b3de5739fbabe568fa55e8e68e59299d5a1fa`

```dockerfile
```

-	Layers:
	-	`sha256:977f62fe6cf30a59c114215d0e2fb07fbb41859ff362f859411e08f5d776825f`  
		Last Modified: Thu, 22 May 2025 00:12:26 GMT  
		Size: 3.0 MB (2988325 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a84f0bee4ef0b993be8d730b99d23ea9d629ed55b61c1b81fa00960f15af30c`  
		Last Modified: Thu, 22 May 2025 00:12:25 GMT  
		Size: 33.5 KB (33509 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:a3ba435a6ca5300c62198ec8b8acbf7e375a384fd9f8d36d6f7c0a8d247839e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70747609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e7a9ba83042323753e2acddba9f6b1c65a43a8b69e5830406d522c58a153b9d1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Tue, 03 Jun 2025 13:37:03 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff357ba464f67422f9bd171700994473e49497437c5ca56a0f7021e263bca8f4`  
		Last Modified: Wed, 21 May 2025 23:17:16 GMT  
		Size: 41.5 MB (41535519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c805703a1dd3d2d49a00ae5a47d47f67f4699cb73d461fe186d9b7390e1133dd`  
		Last Modified: Wed, 21 May 2025 23:17:15 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee39fa726f066a848b80df2af8e01840a2165693f493d9f9f70dd68b991e1b9`  
		Last Modified: Wed, 21 May 2025 23:17:15 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc53f9b1f2e1fc39f917e143bbdfdd766ef5a706ecdac6ae00fa2e0cf0249b1`  
		Last Modified: Wed, 21 May 2025 23:17:15 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6384cb816708865482671f0a7d1a8eaff91f59a3fe5bc9d9693b938c85767a87`  
		Last Modified: Wed, 21 May 2025 23:17:16 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf42d7995e398b787836c23e68e9e7fc1a732ffb96d4fb1685b398d4effaa1b3`  
		Last Modified: Wed, 21 May 2025 23:17:16 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:7060a0a75fc8ed76a78cfacc6452073f985d76c999b3b97e8bb88dced893d345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3034526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01b5f8e208989f3251f894f71c3b418db8ceb0c5e9666b653379bc821b1cce51`

```dockerfile
```

-	Layers:
	-	`sha256:1ea4d8ab26d56d7bd656f2d6851348ab3fc126bb57f1a217617239a460fdd551`  
		Last Modified: Wed, 21 May 2025 23:17:15 GMT  
		Size: 3.0 MB (3001187 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0138efa1caa09d3b9d2ecd650579b9137338da4f6002a46fa0102064f9b87379`  
		Last Modified: Wed, 21 May 2025 23:17:15 GMT  
		Size: 33.3 KB (33339 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; mips64le

```console
$ docker pull nginx@sha256:284f8a3dd1b9aa683e629000a9f9ba5080d22c03956d609a323ff9c32801bf98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68458684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b026702600e9a39fa30a824ccbc9035143e5d5626565050c985189d84605f200`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:48541e37cd82678078df221c38fde515e820c13a623449b699d224f60f15dae8`  
		Last Modified: Tue, 03 Jun 2025 13:38:52 GMT  
		Size: 28.5 MB (28511850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00a6963d3b0df27c574253cf7726396fc59debe62e23e70a59b26c03390d166a`  
		Last Modified: Thu, 22 May 2025 01:00:56 GMT  
		Size: 39.9 MB (39942229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4c209c9a7ecb6398d05421fcf0cac162aff17c9ffc7357dfabb9fca8de8eeb`  
		Last Modified: Thu, 22 May 2025 01:00:52 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb6c26dd38b7be6ebe9dd5331102ee2a8d9b1753dd959bbb3dd2c8026e726c0a`  
		Last Modified: Thu, 22 May 2025 01:00:52 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe5d7f2811a2db658f007b6d21e0bdc159395f90dd0082b8d63819ac4f1bb7d`  
		Last Modified: Thu, 22 May 2025 01:00:52 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff1ce30d1b449e2726a47a47b09aa59f32445e12f9742ac2db31c0a7c815fa1d`  
		Last Modified: Thu, 22 May 2025 01:00:53 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cafbb84a5f710f7d553fc81c26cac89cf3bc036bfb66e0eab371a69b751cef1`  
		Last Modified: Thu, 22 May 2025 01:00:53 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:f44264dc52e1098e34fd09c79c12e046f519e06d96eb8384ac0ccbb75ca22ce4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **33.2 KB (33250 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ffdec67cd54f926a924f3dd92e3c7a1ed68ee35039e5700ee3993b0d27bfd7`

```dockerfile
```

-	Layers:
	-	`sha256:70a2fef795091b19d675f9f6fc05d7210df576e5704d9c1f99b4df9035636528`  
		Last Modified: Thu, 22 May 2025 01:00:52 GMT  
		Size: 33.2 KB (33250 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:79905599c0384a56ef3463fc5cf0ac3a84ff6a66a80c1354511fbaf94eb35b37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77106881 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7546cdf55d7a0eeada2c38d427c881463f4e84a11420b31daacbffb92a275278`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:701606535a7233566815cc9ad5f3e5853b443be5476286f6799008053dc2b03b`  
		Last Modified: Tue, 03 Jun 2025 13:39:02 GMT  
		Size: 32.1 MB (32066912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e293cad5ae9ac16cda5dec53ed0487be51f810125cd01735d1e258821cc985`  
		Last Modified: Wed, 21 May 2025 23:54:41 GMT  
		Size: 45.0 MB (45035364 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:490c7643b8b4c5fbbe58096fbc009007264549a76d2d2f792bd5abca2f9177ec`  
		Last Modified: Wed, 21 May 2025 23:54:39 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ba659b8935778934c9df00b5eda17d080e2b22e872dbf4ba96d632c35ad11ce`  
		Last Modified: Wed, 21 May 2025 23:54:39 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fe1de784de56332e1b56d6325cedd8e30b8e7dda5cdc4357c01629dcd147a2d`  
		Last Modified: Wed, 21 May 2025 23:54:39 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4248356ada3ad819f2353361956ea3bc7d5770507d5c356338b3b693d9216e30`  
		Last Modified: Wed, 21 May 2025 23:54:40 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0637917798d2b9d8486c875f19acfa961fd6a00159701c1659672b86cfd555ae`  
		Last Modified: Wed, 21 May 2025 23:54:40 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:e8f6ddc73537cb08d0fd5a368fc7c994b40957a9444c41c0a7164070e294a72a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3049480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a76413cd6c02eeacf8fc9c056264033a3ea5ba68d3b72bf8721e60be47f91d5`

```dockerfile
```

-	Layers:
	-	`sha256:1932843e425ae47361b8ca916e762960c2673528165a0aca52c767f90e1312b0`  
		Last Modified: Wed, 21 May 2025 23:54:40 GMT  
		Size: 3.0 MB (3016044 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8500661f04db43970f6935b9bbd2d15ee1a2bff2ba53d83f0bb8593f1ed6897`  
		Last Modified: Wed, 21 May 2025 23:54:39 GMT  
		Size: 33.4 KB (33436 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:1c524fde1236d076de1ae53f8db181b168ad30b31151a07d49dfc66456135708
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67073556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87da9be42f691476b331ef3daa36d683d9c9a3077932abe8259dcd02cf83fbe8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 23 Apr 2025 18:00:49 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1747699200'
# Wed, 23 Apr 2025 18:00:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NGINX_VERSION=1.28.0
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_VERSION=0.8.10
# Wed, 23 Apr 2025 18:00:49 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 23 Apr 2025 18:00:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="517bc18954ccf4efddd51986584ca1f37966833ad342a297e1fe58fd0faf14c5a4dabcb23519dca433878a2927a95d6bea05a6749ee2fa67a33bf24cdc41b1e4 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 23 Apr 2025 18:00:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 23 Apr 2025 18:00:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 23 Apr 2025 18:00:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 23 Apr 2025 18:00:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:fb6e196ef379785f6b759a20e90d74fe0566b240771695f724c27a44aa6cd3ce`  
		Last Modified: Tue, 03 Jun 2025 13:31:54 GMT  
		Size: 26.9 MB (26882808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b26b26104ddce741005668fd1259312008704816e0e5950ea99bb4b8f2ad59`  
		Last Modified: Tue, 03 Jun 2025 14:24:48 GMT  
		Size: 40.2 MB (40186154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb82bd31e415b26351686ff705009442c49f302df6cac01b7b9649f21e7230a`  
		Last Modified: Tue, 03 Jun 2025 14:24:46 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37724a0920264eece86d833dc8527e976e9a81aa7dbbfb757245bf2f47ecc89e`  
		Last Modified: Tue, 03 Jun 2025 14:24:48 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b03b129435f64b2a453d4affc125a9d23c6872e7e5b447d292e233a071c502`  
		Last Modified: Tue, 03 Jun 2025 14:24:48 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65cfbdfbdaff6f883b842e4f33fb869bc8e97c1ee9d22c45e3d899e8fdc31b6c`  
		Last Modified: Tue, 03 Jun 2025 14:24:49 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa7df68f118fc898789380a875d0752acf732172bab3d68a3ab37a85a37a90c8`  
		Last Modified: Tue, 03 Jun 2025 14:24:49 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:9579336436a5bcda8fab9867b4ce225f4e8d868bec8a5e5e1a337bfded8dc693
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3032293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceec2641ae5098fd9e8f1c46d63d43203a7a3232f8a32f344adc910b9b2cd518`

```dockerfile
```

-	Layers:
	-	`sha256:fe70ac82b580efa9b02ab8078297f83852e45d8bad323f5db8ab274dc4349035`  
		Last Modified: Wed, 21 May 2025 23:36:26 GMT  
		Size: 3.0 MB (2998912 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f01b8caca885b15360f3b264bb9dce53a5f0ccd58df68bbf5499efec2d65e35`  
		Last Modified: Wed, 21 May 2025 23:36:26 GMT  
		Size: 33.4 KB (33381 bytes)  
		MIME: application/vnd.in-toto+json
