## `nginx:mainline-trixie`

```console
$ docker pull nginx@sha256:c881927c4077710ac4b1da63b83aa163937fb47457950c267d92f7e4dedf4aec
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
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `nginx:mainline-trixie` - linux; amd64

```console
$ docker pull nginx@sha256:617fef3c6adb90788d06f7ebe634fe990a6cd1e63c815facaf5fcaf3fa1ea003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62848827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4af177a024eb8a1e43f4fb6c66735bb8260115cb5925a64f51673219bd97c144`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:56 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:22:56 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 13 Jan 2026 01:22:56 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:22:56 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:56 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:22:56 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:56 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:56 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:56 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:22:56 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:56 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:57 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:22:57 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:22:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:700146c8ad64762607eb0076d9fe376bed85c65f27650a4f3b76fc66f72e9846`  
		Last Modified: Tue, 13 Jan 2026 01:23:08 GMT  
		Size: 33.1 MB (33070548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d989100b8a84afca8cb4b5bcc62beec741cb69e181fe7815d79e4aa04c36ca59`  
		Last Modified: Tue, 13 Jan 2026 01:23:13 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:500799c304244b0545f8f1d54d86d3a17512c219cd0edd3d5f5b60f68f5c6f93`  
		Last Modified: Tue, 13 Jan 2026 01:23:13 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b68cfefee1d8726f1f754e9f566b73bd4df2531476315e6ac55b4fe18e1717`  
		Last Modified: Tue, 13 Jan 2026 01:23:13 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57f0dd1befe210f3a7186fe46ad1552d4bc8864701c8cec580676144bc37d425`  
		Last Modified: Tue, 13 Jan 2026 01:23:08 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf8753feae0b5aaadb86ac2cb972ff57cff12f877ad50c548fde8092e85e7fb`  
		Last Modified: Tue, 13 Jan 2026 01:23:08 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:5e136b60573b2b27f0b5056ff26762298f02562bcb4b118e2bcef24ee8f1d6e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48a3bd2e5be8eb246ca4beeff885913efa777a8d7184dac3be11016e7b0390ee`

```dockerfile
```

-	Layers:
	-	`sha256:785250c9bf9eaa13afc91b2f7d6afb59ab9c2826ecc968de059bedd06f96e9da`  
		Last Modified: Tue, 13 Jan 2026 03:51:13 GMT  
		Size: 2.8 MB (2817223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2dd2dbe62778fed54199f2462c0c5be73c0c3fc536218177eec5a6292a0b4da`  
		Last Modified: Tue, 13 Jan 2026 03:51:15 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:43bb8203632c0eb3c0240c0465c5d1ce707a54ed04793ec0dd56aeded790d929
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54079036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d71ace31fc93d8b0545756000fa58fa2536fe6b36832fb242a4543c2c63997bf`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:25:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:25:19 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 13 Jan 2026 01:25:19 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:25:19 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:25:19 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:25:19 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:25:19 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:25:19 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:25:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:25:19 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:25:19 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:25:19 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:25:19 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:25:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:25:19 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:25:19 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:25:19 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95adc148425fb3f07c7e74d92caad0c0ac97d829505eb25b9507e8ce7c39eb59`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 26.1 MB (26131710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af43b40a59400a90b27770229d5589a0c2be05af1b3ab61a1b51b652a73b1f47`  
		Last Modified: Tue, 13 Jan 2026 01:25:29 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e20b71cf3355035ad9c527cfebcb0f21b48f1bf1c03fb2ee24fa59e26bc7dd4`  
		Last Modified: Tue, 13 Jan 2026 01:25:29 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:722c8ead482d8807c86278717e00d452311439cfa451cffa264e21ace855e5d3`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c388cc12db890fb76218917bf48457a9e65a5a2819e93d2cd0eb33921575935`  
		Last Modified: Tue, 13 Jan 2026 01:25:35 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0ef5626e5e3bbe3041f4fd641f44491abe3305c48d02e9b6fac0b4466e7dff`  
		Last Modified: Tue, 13 Jan 2026 01:25:31 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:7fa8d9f078acdc88ee525c8c2e57899f53b4d3c89eaccb4ef669408823ce2906
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2878647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec7966baa1eb0f1759b9dd6734953ceadb1c047747209a57c8a7a76475331e49`

```dockerfile
```

-	Layers:
	-	`sha256:b7b979690b4d13cdfaa8ddf2ea018b0bf79f91193a3c19292e1e6473f458f1a0`  
		Last Modified: Tue, 13 Jan 2026 01:25:30 GMT  
		Size: 2.8 MB (2843363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f78cbe964c010eecdccfa72fbad3516875ac27055fc80afa56a02d65c411b50e`  
		Last Modified: Tue, 13 Jan 2026 03:51:21 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:2835b6e43f1aea4cd6098fb6cce16078604f5b97907dc2630187d10e19f31bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52278918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ac8b0318df70103d63fdf939bc8bb87f94ced6e455d711d0190967dad2f7770`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:34:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:34:01 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 13 Jan 2026 01:34:01 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:34:01 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:34:01 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:34:01 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:34:01 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:34:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:34:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:34:01 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:34:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:34:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:23 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea50399465957a01892c34a43495d9a92ab44f3f0205f593c9cde637cb007af`  
		Last Modified: Tue, 13 Jan 2026 01:34:20 GMT  
		Size: 26.1 MB (26065744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ccaf4c15d51bbc628a5db223439b1b4a8d656c8542aad1c9fe1161466ccd209`  
		Last Modified: Tue, 13 Jan 2026 01:34:16 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6b48b366ea1bf295a37c9058cba004c8bb28d1cb071c436cf8aace72ea31e55`  
		Last Modified: Tue, 13 Jan 2026 01:34:16 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e74fb25694cbd1476e066ff16962750111a69090eac9edb16c7c3b07a12e6c`  
		Last Modified: Tue, 13 Jan 2026 01:34:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d03e9b5feb0839c4c78a10cbe8f763466749596cb3f97fd9a1dfe3587d97cfef`  
		Last Modified: Tue, 13 Jan 2026 01:34:17 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:538edb91e3dc6bfa8ea96e3397ed559641232159881e2a1b1f4dc1e8bcfa4a99`  
		Last Modified: Tue, 13 Jan 2026 01:34:11 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:2292ae3230a7c1f94ca1ce67db9d1f35d4f5a29dba712e58a989a953596086dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f563c83ba54909f89d399e373edf801fa934b19163e8de8aa94106bde2cd75bd`

```dockerfile
```

-	Layers:
	-	`sha256:6da2732a126e22236a855ba0c27b3ba7a088f080ffc76e026ac425b33a709f10`  
		Last Modified: Tue, 13 Jan 2026 01:34:10 GMT  
		Size: 2.8 MB (2842108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a77556220f49de0c508c0f0fb056148eb34778bc4655da3e6943d88e0cfd472`  
		Last Modified: Tue, 13 Jan 2026 03:51:26 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:378f275f52cbbc5cebdf84b5c4fe51544f28e698e05db75588a82d4cfeb44542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61179182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:904dc4c1bec93e4c618eeb03ba4c47faeaaa7dce860727aad0b2f1682cfb67fa`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:52 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:22:52 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 13 Jan 2026 01:22:52 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:22:52 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:52 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:22:52 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:52 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:52 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:52 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:22:52 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:52 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:52 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:52 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:52 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:52 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:22:52 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:22:52 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15a5b76537aa00de2d2762b3c98cc4df2bd2511a92332e15f90dd6516064d798`  
		Last Modified: Tue, 13 Jan 2026 01:23:10 GMT  
		Size: 31.0 MB (31040546 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c327f67383257c0f0e42d6b29fa44291524a6fb1e637a066ea266df1c0a72`  
		Last Modified: Tue, 13 Jan 2026 01:23:10 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d5a661201446cb1b954925f0f7793803702c6227e879b795bcc48aa02344252`  
		Last Modified: Tue, 13 Jan 2026 01:23:09 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b249cf17a2637f372b686af9ef960b2cc44f5dafcc9841bd055f34ade71166`  
		Last Modified: Tue, 13 Jan 2026 01:23:09 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a178f616fffa69e4b99871d4ef15e93aeb8f189102861dfda888b59fe95742fa`  
		Last Modified: Tue, 13 Jan 2026 01:23:03 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f54f17cce8f7a283ceae266874c54d050acd5713b59b92dcd6a2c7e758040097`  
		Last Modified: Tue, 13 Jan 2026 01:23:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:210a05f6f9d57a0fc6ffc6109c0f9727017832cad74ef0a90d6fc25441efc00b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04a8a08234271bb37202d535f01323b8c3cb615226090faa6193245b6f8bbe85`

```dockerfile
```

-	Layers:
	-	`sha256:f42115329fce567c339a0f3262ada40e5bb114ac5db868956f60bd4824b5acf4`  
		Last Modified: Tue, 13 Jan 2026 03:51:31 GMT  
		Size: 2.8 MB (2817707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ddb646ece5b1eab4cd50fd089c2f3770d8d582337d86796dd51ecbe3709d6e0`  
		Last Modified: Tue, 13 Jan 2026 03:51:31 GMT  
		Size: 35.3 KB (35332 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; 386

```console
$ docker pull nginx@sha256:ccb4f97c5fef6cd5ac731ae0226b9357400a6bfccad41316285a43942015cb57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63241386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df1d6010ceaa6d0bfae40ef7159e6daeee8c275a39c3050cf88d485ae1ca2d8d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:27:15 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:27:15 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 13 Jan 2026 01:27:15 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:27:15 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:27:15 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:27:15 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:27:15 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:27:15 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:27:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:27:15 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:27:15 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:27:15 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:27:15 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:27:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:27:15 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:27:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:27:15 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0885fdb4c79f9beb52c68da572a95df0d882c8a44c857e998a23ab2bdf51a3`  
		Last Modified: Tue, 13 Jan 2026 01:27:26 GMT  
		Size: 31.9 MB (31948308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c99d7bb48ac90200b794f95ec526110c488f531f8c1005e51c92e6035a55b18`  
		Last Modified: Tue, 13 Jan 2026 01:27:25 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0bf8fe35cce1b5997984874c3ecf5efe82b2ede1afbbddf83211cf7919e3d45`  
		Last Modified: Tue, 13 Jan 2026 01:27:31 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:571d46722d594a099ebdee5a6d7ff05c8fd744dcfe59d82bf50bb1e00330fe20`  
		Last Modified: Tue, 13 Jan 2026 01:27:31 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b904c30e3e76738635fca1a2a533ee6f82f356fa8ef26f41598419398d634b1`  
		Last Modified: Tue, 13 Jan 2026 01:27:31 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5ec40da40dd73213b3a3587b8a3e5f4cdbfe2b2dca0852556f73c6d9b8f6b8`  
		Last Modified: Tue, 13 Jan 2026 01:27:31 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:01e442dea1cdd97ab34a5a83f36d5b838aca109de8f8667f608d367f9d453012
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ece621a9200253b79b81de33d91c976efd23e7a7c8e19a0709f2b2ee18e3827`

```dockerfile
```

-	Layers:
	-	`sha256:4f688d082b3ba31909ea5be862cb66fa3c4ad7759b3353e73c8ba9dae3de7476`  
		Last Modified: Tue, 13 Jan 2026 03:51:35 GMT  
		Size: 2.8 MB (2837059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7919f129c58ed774375f08e4f47189a7891476c724a7f15cd0a15932958076e6`  
		Last Modified: Tue, 13 Jan 2026 01:27:25 GMT  
		Size: 35.1 KB (35093 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:3323cdf668da1ce15ad53b115b9e58721ae5d87e493f20d4fedaee926e9dee50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66979643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15f77852ca5909439fa4b2dff3816f7cb7f48660e72df39e413b0899d3f3cf1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:48:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:48:12 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 13 Jan 2026 01:48:12 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:48:12 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:48:12 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:48:12 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:48:12 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:48:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:48:13 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:48:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:48:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:48:15 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:48:15 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:48:15 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:48:15 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:48:15 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:48:15 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:675422c92261454fddf526810afd7e371b0da1c1288cf5df829fa100b282e2dd`  
		Last Modified: Tue, 13 Jan 2026 01:48:42 GMT  
		Size: 33.4 MB (33379441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6292b830822892d70cd441711da96e8bfc26eb2290bbd66efc34acd6e70d6e60`  
		Last Modified: Tue, 13 Jan 2026 01:48:40 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd20a25b37c3d06af1dc120641fc9d9efc8df3a893017ed76e19f9dbc611745a`  
		Last Modified: Tue, 13 Jan 2026 01:48:47 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e774225e60d25882bb558e33b17f8f119c6ea3403cd5ce1b8553aa6fd8f046d`  
		Last Modified: Tue, 13 Jan 2026 01:48:48 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6130426c33ab026fa113fb4f068b0870ad8252f2efaa17d2f0795901e61753`  
		Last Modified: Tue, 13 Jan 2026 01:48:41 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:977a17c024ee69518dc8aca4d906d505de5daf552f73dfb993e022dd0897701c`  
		Last Modified: Tue, 13 Jan 2026 01:48:42 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:44271aebff4ba3c5c5d31645f4a86f83010b8fc68d0fc0d20212eee38cf69e4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2879989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5f482318364c38a59a5cc83c2bd9ea422216acd1469843775c14aac937a8d53`

```dockerfile
```

-	Layers:
	-	`sha256:b3e3f17524499d254e3193e54d792fe9aea881c1d9815b1986b0cd130871265e`  
		Last Modified: Tue, 13 Jan 2026 01:48:41 GMT  
		Size: 2.8 MB (2844753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fe89c9d4b1fe77cd7359d9bf1d836675aa76db57fd01586574166c7a57b94a80`  
		Last Modified: Tue, 13 Jan 2026 01:48:40 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:9d1166a60894763e27289c9adb6a45b2195d465f7e25a596882ef4f5c67143a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57548287 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fdb3784d9efd5db3b42712ffbcae01ba4ee01b6d0d2ed5df95b4839919ba856c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1768176000'
# Wed, 14 Jan 2026 09:27:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 14 Jan 2026 09:27:48 GMT
ENV NGINX_VERSION=1.29.4
# Wed, 14 Jan 2026 09:27:48 GMT
ENV NJS_VERSION=0.9.4
# Wed, 14 Jan 2026 09:27:48 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 14 Jan 2026 09:27:48 GMT
ENV ACME_VERSION=0.3.1
# Wed, 14 Jan 2026 09:27:48 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 14 Jan 2026 09:27:48 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 14 Jan 2026 09:27:48 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 14 Jan 2026 09:27:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 14 Jan 2026 09:27:48 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 14 Jan 2026 09:27:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 14 Jan 2026 09:27:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 14 Jan 2026 09:27:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 14 Jan 2026 09:27:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 14 Jan 2026 09:27:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 14 Jan 2026 09:27:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 14 Jan 2026 09:27:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8c2d1639f4f145e07ecf59940bfa96f17083c024b5c96e8082c50d6075a08b82`  
		Last Modified: Tue, 13 Jan 2026 01:08:06 GMT  
		Size: 28.3 MB (28271687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2471e10a3ba1bb86e7ca2ae452ef57942c397a3848dca56bb2176acba2010ecb`  
		Last Modified: Wed, 14 Jan 2026 09:29:27 GMT  
		Size: 29.3 MB (29271990 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f6d0ce19b25db4bca22497caaf625274b286d4b542b7d8d3adb95f5708114`  
		Last Modified: Sat, 10 Jan 2026 00:02:48 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99540469e7aa67c0fd81390879a959fbf51e392fa4f4293798c8fb00fc9bdb3e`  
		Last Modified: Wed, 14 Jan 2026 09:29:25 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f27a56053e2701acb18f0612825535e01163e14b9bb36439de2aab5a8391919`  
		Last Modified: Wed, 14 Jan 2026 09:29:13 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cc5d1d21c2f1f621443ff0c2a44a43a7c35fc35f37a97d1b30cbe729e87bdb0`  
		Last Modified: Wed, 14 Jan 2026 09:29:13 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f054824f39e4ce6f93b76e31366939fea147dc6fe08a7d1d83fc831d2d3a6f`  
		Last Modified: Wed, 14 Jan 2026 09:29:25 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:aeb3d3b1e334a3a8cbdec39d23c684d28500e1d64fa5105fd22daf241df2cc45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1c0df456388ef6f9a45645aab0a64099ed1f80ae8d40e4811d966af1883133c`

```dockerfile
```

-	Layers:
	-	`sha256:bc3f105d0477f9ea0a9f96eb2d5b9080f3449fc716499088a041d862f1a11d41`  
		Last Modified: Wed, 14 Jan 2026 12:50:42 GMT  
		Size: 2.8 MB (2834540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:072c6a7bde39281504976610188a0a1b88c83d4256c2aa3677565f7a39a91e5c`  
		Last Modified: Wed, 14 Jan 2026 12:50:44 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:550661e3b8aac56093610fecf2a919eeb5bb16e849b446e2f34a5c5f0972a6f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60399324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:175fbeec8858ceeac1488a32b05a503f10ab58d6aed754fe64024108f305cd8c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 14:21:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 14:21:01 GMT
ENV NGINX_VERSION=1.29.4
# Tue, 13 Jan 2026 14:21:01 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 14:21:01 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 14:21:01 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 14:21:01 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 14:21:01 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 14:21:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 14:21:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 14:21:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 14:21:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 14:21:02 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 14:21:02 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 14:21:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 14:21:02 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 14:21:02 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 14:21:02 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2b46bc94baaae0a37e5e04b1babf7e1f37c4390b83d49c3c6820188deba770e3`  
		Last Modified: Tue, 13 Jan 2026 13:10:43 GMT  
		Size: 29.8 MB (29833411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a1be0f0ee1c96a5d1ac079072518cee0e507477ee779c9f6ed6487e9a37446`  
		Last Modified: Tue, 13 Jan 2026 14:21:16 GMT  
		Size: 30.6 MB (30561319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6028771cc3e6597bd1682bc0168d815797f2cde97c6b587ad61e1cc0943770f`  
		Last Modified: Tue, 13 Jan 2026 14:21:21 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cb86e0f7a7984fc38e72b0568e23614d2fbdd002faf0769b823aa4e1413b82e`  
		Last Modified: Tue, 13 Jan 2026 14:21:21 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea0b2f835651cd0648f14079138c87c1302fe926bf92a12c0912865436dcc331`  
		Last Modified: Tue, 13 Jan 2026 14:21:16 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4641bd4fe3fa118f00abb279c271a3f54fe1d31ee69e3080e5dd01e40fb8dd1c`  
		Last Modified: Tue, 13 Jan 2026 14:21:20 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:224105765fbbb86121c5b2f0f483f27b99119cfa96f51a0b681929999619e3fa`  
		Last Modified: Tue, 13 Jan 2026 14:21:17 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:cfe606ff11720098cef73ea6fb20593be5e56e3d111ffb90025e6f2be19a88f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e19752a7d111acc57ced96f3b871bf3b11c182860173bae46228967ecc96cc9f`

```dockerfile
```

-	Layers:
	-	`sha256:4666b45e31c90002a5b0281a2afeebc4276d6d3a51a99b3dee3c1090f5c0d22f`  
		Last Modified: Tue, 13 Jan 2026 14:21:16 GMT  
		Size: 2.8 MB (2750509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:afd8199d9b9bf1f112a4898666f8aa2db074c2d6b34f75ddb0b18742c73f10bb`  
		Last Modified: Tue, 13 Jan 2026 14:21:16 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json
