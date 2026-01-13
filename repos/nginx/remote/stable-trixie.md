## `nginx:stable-trixie`

```console
$ docker pull nginx@sha256:4633bf02d742516967910946e7fe2cf20c8b8b3b12743db1c9edee3e672ecb60
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

### `nginx:stable-trixie` - linux; amd64

```console
$ docker pull nginx@sha256:07019dae7c324421c9193722d274299d8dc352cf108c17d3e904e051a2b8dd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62821574 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94a30ed18e45363486a55379bd1fbb8c479f36524ae816779f3553afe6b787ed`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:23:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:23:45 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 13 Jan 2026 01:23:45 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:23:45 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:23:45 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:23:45 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:23:45 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:23:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:23:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:23:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:23:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:23:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:23:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:23:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:23:45 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:23:45 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:23:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:119d43eec815e5f9a47da3a7d59454581b1e204b0c34db86f171b7ceb3336533`  
		Last Modified: Tue, 13 Jan 2026 00:42:34 GMT  
		Size: 29.8 MB (29773685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:998d5e4721acfcb1f595672abd96e54bb5c606849e71507a3dc44438cbf6bef0`  
		Last Modified: Tue, 13 Jan 2026 01:24:02 GMT  
		Size: 33.0 MB (33043293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d96ce5090ecd8a7100d9c1015f93ab8ebdeed37823c19d54ad4488d28382264`  
		Last Modified: Tue, 13 Jan 2026 01:23:59 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7621fff433f21232e941ca35492d49c1e803a8fa98ad8847b75a145b239008bf`  
		Last Modified: Tue, 13 Jan 2026 01:23:59 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5163318194d9ec539c993586c8f9902455876201450fc159356d2b7277500b6`  
		Last Modified: Tue, 13 Jan 2026 01:23:59 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6697c8ec7c25de13308f9d995ddcc47ff51a4856a64dccad324ec8ff8c298040`  
		Last Modified: Tue, 13 Jan 2026 01:23:59 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae9b786964d090f1b264e950befa57ff94a570299a022a35ccf9d3804f8b5367`  
		Last Modified: Tue, 13 Jan 2026 01:23:59 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:c4b200d3750b1fc6a316bcc60c0c97605b0d9f5559930b66152d075e366f0f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2849980 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb88a901f7c5af9fe102c236b31ab1eb297844ae16d9cba896f874036b85d1c2`

```dockerfile
```

-	Layers:
	-	`sha256:212c51a5503fbb68b53877b4df18b10281cef125b9149117ac37e4a8595b662e`  
		Last Modified: Tue, 13 Jan 2026 03:51:59 GMT  
		Size: 2.8 MB (2816037 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c43a66c8ef20312a823d819a291b75ad0c51705cccb8f87e503bb2c137c4eba`  
		Last Modified: Tue, 13 Jan 2026 03:52:00 GMT  
		Size: 33.9 KB (33943 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:d6c8145e70d90740fc87b5438939def1f223e207be6309cfe4119183dd1e76eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54048593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:129988c881d6396a45f6780e49167bb0715450489be354005bbdc0433ae3f243`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:28:37 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:28:37 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 13 Jan 2026 01:28:37 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:28:37 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:28:37 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:28:37 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:28:37 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:28:37 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:28:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:28:37 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:28:37 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:28:37 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:28:37 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:28:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:28:37 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:28:37 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:28:37 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c113d410d30c2c035a105b56d3937958c81fbe2530f44add3bae903be6864324`  
		Last Modified: Tue, 13 Jan 2026 00:42:30 GMT  
		Size: 27.9 MB (27942724 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acf1b911927b7ff9551ecbd77eacd64baea225678847672316084bd197e3decc`  
		Last Modified: Tue, 13 Jan 2026 01:29:02 GMT  
		Size: 26.1 MB (26101269 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d501876b29b64eb0cbcbd9962b728d559b461809cb874f00a8962da6955b7d1d`  
		Last Modified: Tue, 13 Jan 2026 01:28:53 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:014bcef6ca3c3313fa8cf087bd021770b94bcbd991c4bfaee1534af89cb33dbe`  
		Last Modified: Tue, 13 Jan 2026 01:28:53 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:580925c7f85b83f448aab711700eb490b125395314d7be0fd800aa44f4ca2d6a`  
		Last Modified: Tue, 13 Jan 2026 01:28:53 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48170e2d3240054efc207ac983ef602454377b933849653ed1416029720fd4cd`  
		Last Modified: Tue, 13 Jan 2026 01:28:53 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a892bad3b690b1e5d97c4842ef65c01c97fa4ff0e483b8897399dd74195c1a2`  
		Last Modified: Tue, 13 Jan 2026 01:28:53 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:a39405226b5c5cc073128b4c06a7259c27e682e0fdfb5415dbaebe7e6def4a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18aabfb10dc2603782106cb9dd941751f895b6bb89ad347fae9378fe2c525709`

```dockerfile
```

-	Layers:
	-	`sha256:9155b830453ce83b9a99424fc30ded16f9137e8d8d5da8bf94200ee85649197a`  
		Last Modified: Tue, 13 Jan 2026 03:52:04 GMT  
		Size: 2.8 MB (2842145 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ad99b80842300600b65696d98b446fb260fb1474468def1f75c0ed4e1504c28`  
		Last Modified: Tue, 13 Jan 2026 03:52:04 GMT  
		Size: 34.0 KB (34036 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:1ccd5e6848c801d29a43c199835d3224ef8b5a33a57cd094767b77f5916c83a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.2 MB (52249883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:932df2af9c3975f904bb6bbe15f4f596426255c871253cb0133448a7eedc2962`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:34:04 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:34:04 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 13 Jan 2026 01:34:04 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:34:04 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:34:04 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:34:04 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:34:04 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:34:04 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:04 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:34:04 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:04 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:04 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:04 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:34:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:34:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:34:04 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:34:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7c33f0ee8e5c8636ae24c5685841e42e721bbb2973888f046a05ab9eb619e682`  
		Last Modified: Tue, 13 Jan 2026 00:42:33 GMT  
		Size: 26.2 MB (26208578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904b6a8214a2e1facabca6726ae75d10f945faa2e6cc6dc6816fee1996bbca23`  
		Last Modified: Tue, 13 Jan 2026 01:34:22 GMT  
		Size: 26.0 MB (26036701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3528e1d54de158444779d1fe49c21ece279691566add52e3ed0143bcbf32f3b`  
		Last Modified: Tue, 13 Jan 2026 01:34:20 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0dc1548f2ba87439c5bf5934790e130d642cb10705d44af50c3e72feccff3a`  
		Last Modified: Tue, 13 Jan 2026 01:34:19 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93610aa502352d467cefdd340e33212fefe57805787e5ae019ae2a9f6bb0efed`  
		Last Modified: Tue, 13 Jan 2026 01:34:20 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8aceacbaf427b7728a87c6aadb178a41eb8898fbb4bd79407311b8d9c7bd139`  
		Last Modified: Tue, 13 Jan 2026 01:34:20 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec768f9b50dc7599f205514bddadf2666b5e1f022a098b30dac433bd669568fd`  
		Last Modified: Tue, 13 Jan 2026 01:34:20 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:bb363be5509fbb8d00d531a93093acc7e85e1531d9c8a0de86b5f3c9f0139133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2874928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce272be8aff0c2f2b5687997aa1e7cac589211bd011ef7eec9129ef96f2c4786`

```dockerfile
```

-	Layers:
	-	`sha256:f9dc478f9b23c3a170f67faa8658a0243882e3015cdfed220d71942cda7107c5`  
		Last Modified: Tue, 13 Jan 2026 03:52:08 GMT  
		Size: 2.8 MB (2840890 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ca76b99fe157b24ca64857f8f0005b5a4806d5b33cd954cbbe94874ee34bca`  
		Last Modified: Tue, 13 Jan 2026 03:52:09 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:e9304a167d8e2839ff66c7fb8168d9f913c305fe621ed28b81ebcf3b33a276d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61154146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e4ccf401ba9f89a59873e31faf9ee80cc24b5cb6b8dc15c4e5393551cdaeb58`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:22:54 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:22:54 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 13 Jan 2026 01:22:54 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:22:54 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:54 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:22:54 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:54 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:22:54 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:22:54 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:54 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:54 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:54 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:22:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:22:54 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:22:54 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:22:54 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:d637807aba98f742a62ad9b0146579ceb0297a3c831f56b2361664b7f5fbc75b`  
		Last Modified: Tue, 13 Jan 2026 00:42:49 GMT  
		Size: 30.1 MB (30134042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fe972b68541bdc69d61e29a8cf3d06837c5b206fa34814fafec7756e12191be`  
		Last Modified: Tue, 13 Jan 2026 01:23:11 GMT  
		Size: 31.0 MB (31015512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43c327f67383257c0f0e42d6b29fa44291524a6fb1e637a066ea266df1c0a72`  
		Last Modified: Tue, 13 Jan 2026 01:23:10 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d369a0570c1a2737abe4ecf01b9926b17fa3b9a766ce64f97d95c6e4df49d5e`  
		Last Modified: Tue, 13 Jan 2026 01:23:09 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb30140bca29b0cff9935d7695a36d8d53dabae700e10ac7893b018019d1031`  
		Last Modified: Tue, 13 Jan 2026 01:23:09 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8b766a0c9feec74047fdb191a4042b5a2eaa13a0850467f9f1de0be1eea37d`  
		Last Modified: Tue, 13 Jan 2026 01:23:09 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcc46c200a957fc5929cf86baf37c11850e3a5f5681b04fda4857c0eb9786017`  
		Last Modified: Tue, 13 Jan 2026 01:23:09 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:70c626bbc6f067c82d58d02891958b21bb889922ffe9290c5f86d5ceeed1323e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2850542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e42c5a63b3a5f482f15d00f47c95f978f0e67af4500d82585bca96ce30768fd0`

```dockerfile
```

-	Layers:
	-	`sha256:50f62c9282a8179b7e5e74dddb48a4c94bfad6031b0ba0db534fda4373db0e78`  
		Last Modified: Tue, 13 Jan 2026 03:52:13 GMT  
		Size: 2.8 MB (2816473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99b27083bc3b2cd76d98b6fccdecae5a8783b4fcb83c25811b58c994d7ab2a11`  
		Last Modified: Tue, 13 Jan 2026 03:52:13 GMT  
		Size: 34.1 KB (34069 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; 386

```console
$ docker pull nginx@sha256:f1b9617a3ab997597e6c9def89adb9ed4dbfd2b100317a89f614670392f6ba4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63212500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82993074a751d0d13deede6f52b63e891e036e94adffbbee6a265503e8e3ebd9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:26:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:26:08 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 13 Jan 2026 01:26:08 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:26:08 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:26:08 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:26:08 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:26:08 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:26:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:26:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:26:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:26:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:26:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:26:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:26:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:26:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:26:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:26:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:27bb6d39eda5ced7626db280c3902aacdfade5acd11a16ef9618e3185f69b102`  
		Last Modified: Tue, 13 Jan 2026 00:43:03 GMT  
		Size: 31.3 MB (31288476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3006765a3134dbdbf5398f2eb2863eca23c83e40ea43379ef35a48d65f0540`  
		Last Modified: Tue, 13 Jan 2026 01:26:26 GMT  
		Size: 31.9 MB (31919418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86fd9de13e220024409dd3c99781507167b24448a27a5e4da222abd928bf4f9f`  
		Last Modified: Tue, 13 Jan 2026 01:26:23 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d733fbcf409eaf13d0438494219808d67bba38ee272ee4904c7b3f9fe4c9289d`  
		Last Modified: Tue, 13 Jan 2026 01:26:24 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38d90b864553e0429352bef3e387c57ae12fe0144ab6fb7d71fffe9b779b6cab`  
		Last Modified: Tue, 13 Jan 2026 01:26:23 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca091be7ca78dbc0c312411af4ae1d0bb01fa9d0a7313fe8e5efa812171231c4`  
		Last Modified: Tue, 13 Jan 2026 01:26:24 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9683b9b0eb15f5d0621ad22bd9a6d2a3fadb4b7f67407b36a58fdc487a21ddb3`  
		Last Modified: Tue, 13 Jan 2026 01:26:23 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:0551c79169568e1b3fa0eab7db6622511eb560868154496506eeefc35f7a9c49
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60c5b4d903c99d181afeffd795c9a438556552368b7cda909a680e7f424b9a26`

```dockerfile
```

-	Layers:
	-	`sha256:c5ca775e0e9c89104f828746930d877a46c4b158309e08ecf4b63f36eba0f15a`  
		Last Modified: Tue, 13 Jan 2026 03:52:17 GMT  
		Size: 2.8 MB (2835893 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:816537e3f48e9e0742ca34faf9ea9fd1fc39bc4b28477df1e45452c2eda13a42`  
		Last Modified: Tue, 13 Jan 2026 03:52:18 GMT  
		Size: 33.9 KB (33900 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:dc5fad2664a480e4b09fd59f2b6cc75a92fc11ba51da70c4debfe5282225783c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66950383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5d398c56be87526708d4ec6e36346c78dc71230d4b3c051c8736962a90d96ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 12 Jan 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1768176000'
# Tue, 13 Jan 2026 01:52:34 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 13 Jan 2026 01:52:34 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 13 Jan 2026 01:52:34 GMT
ENV NJS_VERSION=0.9.4
# Tue, 13 Jan 2026 01:52:34 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:52:34 GMT
ENV ACME_VERSION=0.3.1
# Tue, 13 Jan 2026 01:52:34 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:52:34 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 13 Jan 2026 01:52:34 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:52:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 13 Jan 2026 01:52:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:52:36 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:52:36 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:52:39 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 13 Jan 2026 01:52:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 13 Jan 2026 01:52:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 13 Jan 2026 01:52:39 GMT
STOPSIGNAL SIGQUIT
# Tue, 13 Jan 2026 01:52:39 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9a275bb13cf8b3e9db52a41b6b4ff22ee1ffed00394f6deddd2de45044bd3bae`  
		Last Modified: Tue, 13 Jan 2026 00:57:13 GMT  
		Size: 33.6 MB (33595600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d3d4ea1bcd3d9d3286ddd5b5d6b1bcd042be7036dfeb48535991cca61b2ebec`  
		Last Modified: Tue, 13 Jan 2026 01:53:13 GMT  
		Size: 33.4 MB (33350180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f382809c72e76679ed8021b396d9bdbf47f14c6f37b7d50cba54b614b857614`  
		Last Modified: Tue, 13 Jan 2026 01:53:11 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f5fc43cc30e9d88a434d5c5f4558ce1fcb69e8f80c57152670dcd5ee6777efa`  
		Last Modified: Tue, 13 Jan 2026 01:53:16 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39e67be9fde0aa86059214bcc959d6363a0be9bcfe1c58b624ce5613400b0ceb`  
		Last Modified: Tue, 13 Jan 2026 01:53:10 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cea529cc5257dc48ccfd205a30a87c303c48be6a8f071c501cd14b660bf6914a`  
		Last Modified: Tue, 13 Jan 2026 01:53:10 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f391b4607e2add9d459e86e0fbb7db1bf73f93308c08c3f83a4cfdc78420929`  
		Last Modified: Tue, 13 Jan 2026 01:53:10 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:ab0764dd69f007705739bc941c4dee66cc5cf0d22042e4996ff36e099d58994b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c02d6ae15f74fb06623054eedf4725ff2d1393930ff4e5d36f244cff6318669`

```dockerfile
```

-	Layers:
	-	`sha256:cf9e2fe723bbedd6df4490cfb4870662a376786175b4d9a9619ef770d8d87522`  
		Last Modified: Tue, 13 Jan 2026 03:52:24 GMT  
		Size: 2.8 MB (2843543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b837385e5afc68872305126c4e7be37fac432653ff1bc507b372a005fa8dada5`  
		Last Modified: Tue, 13 Jan 2026 03:52:25 GMT  
		Size: 34.0 KB (33998 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:4a4e5b223eea4713ba88d7a8a7c80c20cf23496fbb3e4ee36e59ebe19a284be8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.7 MB (54680875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071369d881f33b552c56cdda55e1f8a1664ca170a47c75e804739c488751cbf2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Tue, 30 Dec 2025 08:13:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 30 Dec 2025 08:13:24 GMT
ENV NGINX_VERSION=1.28.1
# Tue, 30 Dec 2025 08:13:24 GMT
ENV NJS_VERSION=0.9.4
# Tue, 30 Dec 2025 08:13:24 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 30 Dec 2025 08:13:24 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 30 Dec 2025 08:13:24 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 30 Dec 2025 08:13:24 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 30 Dec 2025 08:13:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:25 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 30 Dec 2025 08:13:25 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 30 Dec 2025 08:13:25 GMT
EXPOSE map[80/tcp:{}]
# Tue, 30 Dec 2025 08:13:25 GMT
STOPSIGNAL SIGQUIT
# Tue, 30 Dec 2025 08:13:25 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9bb01b00c6a6116152fa50d416897aa6976c014d4b0cb5f7a3f7f61aefbd8e4`  
		Last Modified: Tue, 30 Dec 2025 08:15:01 GMT  
		Size: 26.4 MB (26403135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69004e499cb8b74bf07a31b6fcafc1a95ae6600653bb84b5fd24f23b8584ed38`  
		Last Modified: Wed, 24 Dec 2025 10:24:15 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40556089a349428f49a73b68585f186724f7e9bb3600157b55a58b5399f9aa57`  
		Last Modified: Tue, 30 Dec 2025 08:15:00 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2342f66cb613c38fdc6e1b35b9085e4d0be036bf2beed2e64800eeb702c7b99b`  
		Last Modified: Tue, 30 Dec 2025 08:15:00 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:caaa6d933cae498ce1e55ae815ff971b9b6adc01d7d2875dde2cc55e5c2cae44`  
		Last Modified: Tue, 30 Dec 2025 08:15:00 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91a30a5475ac828a97d58493ecfb54de35ed14032cfaef262ae9bfd0864c63c5`  
		Last Modified: Tue, 30 Dec 2025 08:15:00 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:1d00db3ab39a123a60b3b3bbb9ca6dd79198f46c1e2a49140228c7bcf1ccb201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2861275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:008fa9db43ae0bce0527c80772532e0061a3c54eeeb4c415cab610631be635df`

```dockerfile
```

-	Layers:
	-	`sha256:de83e9266c1ed576dae353179bfa07f29e92ff96c0f47e9d20825d4649f9f0ca`  
		Last Modified: Tue, 30 Dec 2025 09:51:00 GMT  
		Size: 2.8 MB (2827888 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f53f93b390c857a665fc90e3c2d9134f0261c97777fffe31573f7e8e09b78fd`  
		Last Modified: Tue, 30 Dec 2025 09:51:01 GMT  
		Size: 33.4 KB (33387 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:8e8782229f455647a99b2e62195cb75447c37bb4434e14b5c1517acae4daad00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60371597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4f3fb0b29ee37e81eb5c3d32d176b188750b4141c08013d61ba18d6b8d7141f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:59:59 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 09 Jan 2026 18:59:59 GMT
ENV NGINX_VERSION=1.28.1
# Fri, 09 Jan 2026 18:59:59 GMT
ENV NJS_VERSION=0.9.4
# Fri, 09 Jan 2026 18:59:59 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:59:59 GMT
ENV ACME_VERSION=0.3.1
# Fri, 09 Jan 2026 18:59:59 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:59:59 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:59:59 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4d43d5eadf39a2428e91a4e6fde0188f1cfb76354598d818d2ef2f8ff5cfa8d65993248b19a2d7ae663798d2362905e63ebd5dca6ca82cabc2831631d0e079ea *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:00:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 09 Jan 2026 19:00:00 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:00:00 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:00:00 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:00:00 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:00:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:00:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 19:00:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 19:00:00 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64ef08d54866f87e562cc7e555b832c2cfe1d007c6adebd982f339ab8e445fed`  
		Last Modified: Fri, 09 Jan 2026 19:00:28 GMT  
		Size: 30.5 MB (30532575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6273584f4fa5f78072968a07f49ecb693a39e38485a7a7d89e08e2059ead4ab`  
		Last Modified: Fri, 09 Jan 2026 19:11:25 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfe0d6c6629df4640a2b4749cdf16033c41b8b36c80294ca74b6c73f6dc38992`  
		Last Modified: Fri, 09 Jan 2026 19:00:25 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2536c57b64099d0c31238831215e0cca2b77c8e21743ec6860f26e879463d058`  
		Last Modified: Fri, 09 Jan 2026 19:00:25 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dcfdff00b17225eb3b8b5e1ed6860ef96703b323cbbd5a32495ae04cbe9fbb8`  
		Last Modified: Fri, 09 Jan 2026 19:00:26 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01244a868f8f073471bd0436f2df1808d13c88e6d739c1217cc4b1f78fb4b811`  
		Last Modified: Fri, 09 Jan 2026 19:00:25 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:503c65c9a6cb41d025c7282cdbf2041ca24987ca330bd56e6f93ac4e6e8049d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2783168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9aac7693b13e84f582d56c2aa973450f56494c1b35d61280fcb17ddc6893aa`

```dockerfile
```

-	Layers:
	-	`sha256:eb1eb595eba391392f1d99dcf08580dd98011439f4c78d87ade4146c7b932b10`  
		Last Modified: Fri, 09 Jan 2026 21:53:46 GMT  
		Size: 2.7 MB (2749225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1610f29f5bb4abbd4f057ff3445723a5bbacb8171ae11e279bedfb17ddc9dae8`  
		Last Modified: Fri, 09 Jan 2026 21:53:47 GMT  
		Size: 33.9 KB (33943 bytes)  
		MIME: application/vnd.in-toto+json
