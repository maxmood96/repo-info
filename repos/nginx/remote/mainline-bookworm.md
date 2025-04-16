## `nginx:mainline-bookworm`

```console
$ docker pull nginx@sha256:81a3df1d6195a1318d4821f59f8a6a20e3c6ea2775eeab9bd3c5a33346479e84
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

### `nginx:mainline-bookworm` - linux; amd64

```console
$ docker pull nginx@sha256:69747b174b56bc170ca99a6d8e7a80e77a020c9702dda7e44a2154066a7a4dbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.4 MB (72382175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e1b6bae1e48cdbde8e6ec3e6ee42d86ad4780156e75790465bf6fb16c551c27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:8a628cdd7ccc83e90e5a95888fcb0ec24b991141176c515ad101f12d6433eb96`  
		Last Modified: Tue, 08 Apr 2025 00:22:58 GMT  
		Size: 28.2 MB (28227259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0c073cda91fdc0aac18d3b7ad19faeea4c3e1f1e45c8e97256410a580d48bb4`  
		Last Modified: Wed, 16 Apr 2025 17:02:14 GMT  
		Size: 44.2 MB (44150318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6557c42ebeaea010d8a8883fdacdc5a17dea1221416d0d980e206dd42dc7e29`  
		Last Modified: Wed, 16 Apr 2025 17:01:52 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec74683520b9c235ea1336a5165c6118a35cacd4d9878893a36b506b89334c50`  
		Last Modified: Wed, 16 Apr 2025 17:02:13 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c95adab80c5df4140fa3f348e07f127ba6f5c2a9ed8637cd27d5a5be5010330`  
		Last Modified: Wed, 16 Apr 2025 17:02:13 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad8a0171f43ec421ec572495b70d68bfd77b63acd094e4a4af794cb427516246`  
		Last Modified: Wed, 16 Apr 2025 17:02:14 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:32ef64864ec3b7cd667027631b05dc66a5fa40b05affe0e74a1bd01d1d57d6e5`  
		Last Modified: Wed, 16 Apr 2025 17:02:14 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:aa00af812341e2e31979c68e5eed4c804c98edeebb4ddaee0d4a4c00cc22d797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5914cbaa80aafe48b6519255eab7191b0c33a9b30ab4144307cbdfeb005a07b`

```dockerfile
```

-	Layers:
	-	`sha256:8273a668194faa4169c525c2364de111cebf22b3c14396731a05ecfe32ba11fb`  
		Last Modified: Wed, 16 Apr 2025 17:02:13 GMT  
		Size: 3.0 MB (2957468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a9f5feb08cec1ee6159fdcbb3e72a95fb364801338570b4d4f71a6236a80727`  
		Last Modified: Wed, 16 Apr 2025 17:02:13 GMT  
		Size: 34.6 KB (34602 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm variant v5

```console
$ docker pull nginx@sha256:fda00832dab8542c951b6e894518272798a53156a552100bc93f85b69a1c14fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.8 MB (64778175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0967af4c641f5f57c80cc51c6b30a0fc237e6a81a7f1bd60c3612ec5d0218c9e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1743984000'
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
	-	`sha256:bee0b90cda85f033e5343bbd7872c95c9de54d2dbe2fe864e9cb4b10716bc994`  
		Last Modified: Tue, 08 Apr 2025 00:23:07 GMT  
		Size: 25.8 MB (25757818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73006efb32249eaae6a67ad17624e139ae583c44941925fe0697fe86e0509a81`  
		Last Modified: Wed, 16 Apr 2025 17:07:14 GMT  
		Size: 39.0 MB (39015760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:959492914ce2ed80e3db96e1b646453be818a9eeb1168f2df29679aa9f73292f`  
		Last Modified: Wed, 16 Apr 2025 17:07:12 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fb9b31ee9eb682710128641d03996d2e43f75263c0b1867942a7d3e942a016`  
		Last Modified: Wed, 16 Apr 2025 17:07:12 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0c6e12c0a300b8ef4a90b1e524ca3d8338a06dbb719e624f46f094355ced73d`  
		Last Modified: Wed, 16 Apr 2025 17:07:12 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48a9c10978d1f296a6ef1ffc26eb013fe6aeef4c496f4c4d3f9d4911bb824ab0`  
		Last Modified: Wed, 16 Apr 2025 17:07:13 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be25e0a1104a2720c0b32c1dc55e9cbfd4134c3a1bb041b8af4bbfee6e14a2c5`  
		Last Modified: Wed, 16 Apr 2025 17:07:14 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:77c42b0a84f0f21c41380b5631887744506a2f72997b8afb6cdc5e8f4b978f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3013417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b9d88ed86abf8a5d844285131529077773b31b07a57b99ef32798924ee996df`

```dockerfile
```

-	Layers:
	-	`sha256:1c0b73c9e8e9536b2bb850191f2f2a17fb577ae007c9261df4a00120e2a84e84`  
		Last Modified: Wed, 16 Apr 2025 17:07:13 GMT  
		Size: 3.0 MB (2978691 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:213135d5e536f097543f354588caa36176906730d36005b1a30a23b543baf89c`  
		Last Modified: Wed, 16 Apr 2025 17:07:12 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b9a2fc7f1fac1ab3908ea4d4760ba5d54982e9b241943d2ea84a90c022979de8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63016915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:899ab6ac2e6dcfa5438155603f8d99b575d93183ec108a1f4edea62a34e3301d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
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
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cfa44eeacb64e9b57de04fbdf716c439ac36c0a213ed0cdff27ee3c467fc0a`  
		Last Modified: Wed, 16 Apr 2025 17:06:52 GMT  
		Size: 39.1 MB (39074449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e09b04cc00de8e4dec63e878994eb872f9102317cbb76db4c96930204ebdc0`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5275e540c28b729e385c7620813f7de9287a7292786ce73b634e2186066b849`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0d51b78ee783d54a5c1062270f51e233b68c6352a8b1d094eb027bcdbddd04a`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3091d454b2dd1e26aacd5861f0edf3d1e524b63ac7875ec4079b08781f9fde`  
		Last Modified: Wed, 16 Apr 2025 17:06:51 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9ef3c4318b9248d6e3117d08e3fe2d886db07f820d61e4c9fe8f834c89dd0ec`  
		Last Modified: Wed, 16 Apr 2025 17:06:51 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:24f43b83a0358be1e0be6b3e02dfe27c6f8b1cf5d6ad445f5205df18eae18a09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:006e1b9c22f7312ad3183db57599021703f194c66f6c93da93acd34d99c23a1d`

```dockerfile
```

-	Layers:
	-	`sha256:ae0806474b73a027b0c9962d6d003b3429b3595dd1393914633fa9d38513b317`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 3.0 MB (2977658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c787df3479e532412add9667a76b14ad8e8ce5038575870b6b667ba911c039d4`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 34.7 KB (34726 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:a70479423a2f7cfe7f3fca625ed0a2988947f0dd78f091ea89057b2855b4c2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68823226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f94323bafb2ac98d25b664b8c48b884a8db9db3d9c98921b3b8ade588b2e676`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
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
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de29066b274e2ed2dac558eef4fd46026fc03a8ff10f161d9909224984e689a9`  
		Last Modified: Wed, 16 Apr 2025 17:01:35 GMT  
		Size: 40.8 MB (40752310 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf157fc31fe8cc4501ab2599d6e2364defae458486140e6c3612dc321882b07`  
		Last Modified: Wed, 16 Apr 2025 17:01:34 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45096856395554482df00dc06f6ca412312afdce69f02c8d34b7482f309d5cf1`  
		Last Modified: Wed, 16 Apr 2025 17:01:34 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b14c47aa231e326ee90e85d440f0007c902fd4b4c27d0d2f7a747dad7fe2939`  
		Last Modified: Wed, 16 Apr 2025 17:01:34 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8a9ced98467386fb8929b6d25a8ccd4d6e835370c456dc6e6d97155c98d1ca`  
		Last Modified: Wed, 16 Apr 2025 17:01:35 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96c7b918bd5e8a6966d3e2b1d2ef2a284459902d33f7539fa3531cb13c7dcc7`  
		Last Modified: Wed, 16 Apr 2025 17:01:35 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:d0cd4c1cf74d942794561ff7c4bfe9a0d46c241190ca736b51bbfbd3f20bc9be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2992697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf95309d28dec9477c68e26d544fbe2fbc93c901830d96218b37414a40f221b5`

```dockerfile
```

-	Layers:
	-	`sha256:44ab9f01dd12ebb6a761aa768a90c8b6a1c68ed8286fa2460ca169b619da9cef`  
		Last Modified: Wed, 16 Apr 2025 17:01:34 GMT  
		Size: 3.0 MB (2957919 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9b92c591608683331dc3996519aa8fd438015c99b79505357cb138051cc3eab`  
		Last Modified: Wed, 16 Apr 2025 17:01:34 GMT  
		Size: 34.8 KB (34778 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; 386

```console
$ docker pull nginx@sha256:babad783dca44e555a1d3892a462bc798b2eb3ac462be93da8bea9db344f8bbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73201223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f17b290fcc59b4b7f6fc9c4e61a61b6ae4a2f20f4d9aa524c370eca08dfc6063`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1743984000'
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
	-	`sha256:e4fab02059329179b6416bda7cdc389d26699f1c93a02194f146c047031c4748`  
		Last Modified: Tue, 08 Apr 2025 00:23:49 GMT  
		Size: 29.2 MB (29210731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:713b2a178950c33a398eac595c03a706915062a192959a1bf84ccdfba5d81a0e`  
		Last Modified: Wed, 16 Apr 2025 17:06:51 GMT  
		Size: 44.0 MB (43985891 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a901753f7a5fa5082be5efc261f6ef14bdefb3c42cb12ba9459bf4a72fbad20d`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25f6c9751e4d2fd13a8e96664d12fbd60e4aec20ef9a014b5f48b7649a2813da`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b62fc1d277c46ae1a3e7465f1e3c3e88d502b58a1ae924000d741f607bda6b37`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64f76e2049b1b6b9a9b8fcf68de2b157e5c31245e6064647548ad1f9bfab449a`  
		Last Modified: Wed, 16 Apr 2025 17:06:51 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61d9fbd5e25b39da0c623762c81e8993b031df4153602f9767966ecf788d0ca`  
		Last Modified: Wed, 16 Apr 2025 17:06:51 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:734f534a877e0d887ead5b27f86ef1c656b7e4e237e24b5db26c656205218efa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3005279 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c4023579bf3628db42e9c528a0cae7892fd19382285edd66c45adef292cb8c8`

```dockerfile
```

-	Layers:
	-	`sha256:3ee3a17540ab73ed1320cc38565fb6afb20111daff63bf3115fb99af7cbd0469`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 3.0 MB (2970739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a3c6de13375fef5af626d4eeaacc071df3844f84a01cfe6c71828e5b2f7857f`  
		Last Modified: Wed, 16 Apr 2025 17:06:50 GMT  
		Size: 34.5 KB (34540 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; mips64le

```console
$ docker pull nginx@sha256:4a2475325e9bfd3afe7072826692a96265d3f8d21998f2053c1cfa4cb10ead7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68274249 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be11817249079aa0fa2491b9433cc386cd8a53aca9b26f72bed87bd11a53c118`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1743984000'
# Wed, 05 Feb 2025 21:27:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NGINX_VERSION=1.27.4
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_VERSION=0.8.9
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Feb 2025 21:27:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c5170849255c666bce01dd02c1afbe442b1ecb682c342680d91dcd7cd477b57d`  
		Last Modified: Tue, 08 Apr 2025 00:23:28 GMT  
		Size: 28.5 MB (28513953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea31f06f34df1488d58de2956fb3acf7ac0c5f2c283f023fbd52573abebd297b`  
		Last Modified: Tue, 08 Apr 2025 02:47:33 GMT  
		Size: 39.8 MB (39755695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0b99aed50cbc253bf3ec2eaad66ac51aebb3942374cdec38175a6367c30da9`  
		Last Modified: Tue, 08 Apr 2025 02:47:28 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0fd2b4e601bf504c335ff6be2ede03cdb80b1a19d95a5627462aa7f8eb140e6`  
		Last Modified: Tue, 08 Apr 2025 02:47:28 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81f24faf9dfb666c985fd99413ce33c2b7677dee53f4cda424842fbb9e43a284`  
		Last Modified: Tue, 08 Apr 2025 02:47:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e20f5b2c317c3826d7e070925f8ab143bc2c34e72931de0d87ecde0697b3937`  
		Last Modified: Tue, 08 Apr 2025 02:47:29 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acab381d1073a5a8375f6cb2be495f6c747bc563f90c12882943b90261a7b29b`  
		Last Modified: Tue, 08 Apr 2025 02:47:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:291f0ff112d6349f8e911e085ec08fd8573fd7cd2efe786dce2e2ec12edaa221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0b3214bb779d2a497d19a7e44fc31704d41092bbf329cd0f356f014570969a`

```dockerfile
```

-	Layers:
	-	`sha256:474476d22becccd19cb39ca0589d3b42cf4ea810ef2cb9f1cad306ebb412eaff`  
		Last Modified: Tue, 08 Apr 2025 02:47:28 GMT  
		Size: 34.5 KB (34524 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; ppc64le

```console
$ docker pull nginx@sha256:fddb0f09b70b961b484c8694006384c04e245b4f8c35f28cc1e93ac89b34869d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76890097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b0d97b6890e424f75297641fb7a8411382f169db97f03573b1ce4863beab029`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1743984000'
# Wed, 05 Feb 2025 21:27:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NGINX_VERSION=1.27.4
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_VERSION=0.8.9
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Feb 2025 21:27:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:eda04574e09a8e08ba343dd01ac61bceb64282d2e992a997bd2102897b52d004`  
		Last Modified: Tue, 08 Apr 2025 00:23:44 GMT  
		Size: 32.1 MB (32068231 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e2f17e6df070a9c64df41079670d2212d5b3343789f27c6fb44f59a73885af1`  
		Last Modified: Tue, 08 Apr 2025 01:57:16 GMT  
		Size: 44.8 MB (44817269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:398ecd0edc0743d8a32a17bd973e81fe4e4674e68f7368b742cdd42ae2bb5130`  
		Last Modified: Tue, 08 Apr 2025 01:57:14 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab66f52734ddc3bc139ac45aff6bf943fb51d0b5d5f2f092fa81ea543205b5bc`  
		Last Modified: Tue, 08 Apr 2025 01:57:14 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2039d19d3cca3b847adce7d1e75ab6624c7cd66d002e4c1e1977d10fc375c066`  
		Last Modified: Tue, 08 Apr 2025 01:57:14 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8858458e5e05052c659990b67422b9caa8f2eece1c9c0069b69a626fe9a0400e`  
		Last Modified: Tue, 08 Apr 2025 01:57:15 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dab4b1cc96320a6d0bfc64cb3d69e6b86b02c00a2a4840cdcd6d27b3a0335e26`  
		Last Modified: Tue, 08 Apr 2025 01:57:15 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:634af8de5bdf18b1f6ff5614a6cc7a082d2390efa28f99f1dae67cab60713288
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3019946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a69569ace73eddf6e7b9a75974b6aac3b40f7cef0f7b8dd93b6b605804475203`

```dockerfile
```

-	Layers:
	-	`sha256:6158f51db5f617f6bcb74f5b8416da3a98a0947743569728a299edf804045d76`  
		Last Modified: Tue, 08 Apr 2025 01:57:14 GMT  
		Size: 3.0 MB (2985247 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aad44cbd72bb1e8a86cf07833dd8982af80389abc75f2e03ed348c83340c47c1`  
		Last Modified: Tue, 08 Apr 2025 01:57:14 GMT  
		Size: 34.7 KB (34699 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-bookworm` - linux; s390x

```console
$ docker pull nginx@sha256:a99b7d9812dbb7527eab8161807e879c3e66951ddccf21c5302061a651289da6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66884309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89c0f200433569139d9d1fc578b848e0934751ceebc42a22672b4a96edc3f41a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1743984000'
# Wed, 05 Feb 2025 21:27:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NGINX_VERSION=1.27.4
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_VERSION=0.8.9
# Wed, 05 Feb 2025 21:27:16 GMT
ENV NJS_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
ENV PKG_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
ENV DYNPKG_RELEASE=1~bookworm
# Wed, 05 Feb 2025 21:27:16 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --export "$NGINX_GPGKEYS" > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ bookworm nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="973690e64fa47e3704e817a3b08205b9e3f8c0cbe31825d9d62a81c11eb3aa186df015f27fdfd48c8799ffc528e38a9168c592ae665e4835c2d28638ec5f7845 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 05 Feb 2025 21:27:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 Feb 2025 21:27:16 GMT
EXPOSE map[80/tcp:{}]
# Wed, 05 Feb 2025 21:27:16 GMT
STOPSIGNAL SIGQUIT
# Wed, 05 Feb 2025 21:27:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4d39bd57bcf7f4854587de5b4defd11e1b3b354bad1320b74c6994d07d7b3671`  
		Last Modified: Tue, 08 Apr 2025 00:24:14 GMT  
		Size: 26.9 MB (26884606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6ebff784c3c7fbcc69a2b5d8213baa056b1638c508cf9431580bb91acb21162`  
		Last Modified: Tue, 08 Apr 2025 01:52:35 GMT  
		Size: 40.0 MB (39995104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc90c60596a996df8f55a10ba7d7ae66cbdec9f195c4162fbc758f675266ecaf`  
		Last Modified: Tue, 08 Apr 2025 01:52:34 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08647f71e4a764b7c447ade9726123212556f3e1758fcb2c4777f4e8a5a01c60`  
		Last Modified: Tue, 08 Apr 2025 01:52:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0103293170e171005b18c20ed5aaa18365980fa4f77878f34815994f33335d4e`  
		Last Modified: Tue, 08 Apr 2025 01:52:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ca0524884c90a013bdbfd7216b27112418c1cce7a23d5c96ea90fb5247b283`  
		Last Modified: Tue, 08 Apr 2025 01:52:35 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2ec02a622ab5e4a1df83cd19efb2009f01d4c878103f161324e83da21145a8c`  
		Last Modified: Tue, 08 Apr 2025 01:52:35 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-bookworm` - unknown; unknown

```console
$ docker pull nginx@sha256:a1e6f44bc7da1981130e18b36c1429d2a436a068642853d67ba36eaab952a2c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3003478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4708ae70e226073b8c46197fee27ea368f5484cbf75a963f15fd5c07d8c66fb`

```dockerfile
```

-	Layers:
	-	`sha256:b6bddc4f7302ce94d9fdf41f11abe1803e74632c72d6c69f3b00d87e6d4f4e82`  
		Last Modified: Tue, 08 Apr 2025 01:52:34 GMT  
		Size: 3.0 MB (2968859 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e76662905bd01ffae6b883529c29cce7e3213082286f0c24ef49d61aa69208ff`  
		Last Modified: Tue, 08 Apr 2025 01:52:34 GMT  
		Size: 34.6 KB (34619 bytes)  
		MIME: application/vnd.in-toto+json
