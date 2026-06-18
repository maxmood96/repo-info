## `nginx:stable-trixie`

```console
$ docker pull nginx@sha256:175358c3ce472b488fe33f3088d80b3b52d682a45b0487eaefd05f57f07c61b0
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
$ docker pull nginx@sha256:1e1e4509fa2528e8b8237c56cf713a99c0cbe045ce2902f3e2be57413732d393
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63090143 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7a9d08bdd334b64180d6c910b3f39b223d1743c37b82f715ad4456348d2e790`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 22:44:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:44:51 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:44:51 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 22:44:51 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:44:51 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 22:44:51 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:44:51 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:44:51 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:44:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:51 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:51 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:44:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:44:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:44:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:44:51 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58b02fed4ca89539d26f64a999d504c0fc8aa8dc7b3a6344378e13a2a818df96`  
		Last Modified: Wed, 17 Jun 2026 22:45:02 GMT  
		Size: 33.3 MB (33300134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca166020296c7fd9698340d3462aedb904e95599b6969cf072e4330bb328e18f`  
		Last Modified: Wed, 17 Jun 2026 22:45:01 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18b49884a5e029db9a7e5ae03bd8e97625356099b721cc45b8cd98dd12bb2b2f`  
		Last Modified: Wed, 17 Jun 2026 22:45:01 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2885986b77f7f2d417fe9e36904dd8a4005ec37426d53eccc1b223d3669bd959`  
		Last Modified: Wed, 17 Jun 2026 22:45:01 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfadf2ce4af5154a891452555afa420457f6836430b31e83421f9a44bf97b660`  
		Last Modified: Wed, 17 Jun 2026 22:45:02 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b54043d07a8d047a58b1a0b1fcb7ec92b1fd5ebad425209b5a57a9922e41a21f`  
		Last Modified: Wed, 17 Jun 2026 22:45:02 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:6123d179d099e7301518d7a8cbe437a6023c46357e9b7533e60a2f071082316c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2850238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a5cb301bf999d4ff3b1cfb8719c4cfcb89fea3249ec05dee8c6e6d10433a42b`

```dockerfile
```

-	Layers:
	-	`sha256:42a68a0b4921d5ceecd3854535e568a5a2c294f1a0ce1f0d4d5b33a9f7d16581`  
		Last Modified: Wed, 17 Jun 2026 22:45:01 GMT  
		Size: 2.8 MB (2816297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:07aab42f51f743160fb6350994a60c51565c4eb3450c2d1b6311a33ea500f56f`  
		Last Modified: Wed, 17 Jun 2026 22:45:00 GMT  
		Size: 33.9 KB (33941 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:5a02c66edfcbbd3a541bec290731041729077f43bc0a21f000a68d8c529fa069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54249595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca3787ec116787a759ebb0f0101fee899d9d137d2b3ee64411e494264830e83`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 22:39:30 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:39:30 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:39:30 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 22:39:30 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:39:30 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 22:39:30 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:39:30 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:39:30 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:39:30 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:30 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:30 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:30 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:39:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:39:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:39:30 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68dca08363ee9e44ad62339c6a85b834f90f01e984002b07f2641f4af85fe1b1`  
		Last Modified: Wed, 17 Jun 2026 22:39:39 GMT  
		Size: 26.3 MB (26285786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df7dce995a857a39a62155046ef7d3a55414d08b550a7450b9851627edbdbdb1`  
		Last Modified: Wed, 17 Jun 2026 22:30:37 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2eecb4be020e79aefe1af9d8de616cd8e99c1f8ab219d8b6816efe4842ce91ee`  
		Last Modified: Wed, 17 Jun 2026 22:39:38 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38bfae64586e77777abd542e1e3356a163afbeab21e6d78a45aa4fd6e4e64f2d`  
		Last Modified: Wed, 17 Jun 2026 22:39:38 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f200e287b27ce89ca050fdd25be15bc9ea8f0f571d259ef8c4e9b2a8b17a0968`  
		Last Modified: Wed, 17 Jun 2026 22:39:39 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b46ab95f772dab456b99c268affd5d94ba33b69b545557478112b1588cf2592d`  
		Last Modified: Wed, 17 Jun 2026 22:39:40 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:175c4454f95e1df586ac5d515a240efeff7e476a0d5f31eca7e2fdd3541f4297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1add1d9cf469188c831074737402266f35cbe2317e4f1abaa6ecf7a09616515f`

```dockerfile
```

-	Layers:
	-	`sha256:9257ea494c697fdf89bc88585597b7c1dae321f78b55265853a32c9dab38fe9e`  
		Last Modified: Wed, 17 Jun 2026 22:39:39 GMT  
		Size: 2.8 MB (2842405 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79a1cee2819f8af0f26f619f25a74007b30bc894e32ed69137d1af01bccb418a`  
		Last Modified: Wed, 17 Jun 2026 22:39:38 GMT  
		Size: 34.0 KB (34039 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:4f700623f821f223f1782c5f0325045f1eef61bb98324c02cf89fe29fee0146c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52447755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:830d2bb27a9352757a59e8dc20d6aef5375272602b3eda37321080937bc03101`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 22:39:23 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:39:23 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:39:23 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 22:39:23 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:39:23 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 22:39:23 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:39:23 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:39:23 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:39:23 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:23 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:23 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:23 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:39:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:39:23 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:39:23 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:39:23 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a967ef376fb95f9d12daea51b9651adcb9b0ca90c94b4034f111efd6b1aef400`  
		Last Modified: Wed, 17 Jun 2026 22:39:32 GMT  
		Size: 26.2 MB (26232149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12a084f4eece49e635fa78fba7deaba8b7e41fb54fae61fe8c56e581e8b4749c`  
		Last Modified: Wed, 17 Jun 2026 22:39:31 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27923a04426da4315aa60d799a8b38b96a8e615b519a34f13e6b66b2e19e7d5e`  
		Last Modified: Wed, 17 Jun 2026 22:39:31 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f2266cf768ca2768f17831f38413b64034cc7b20893e1d0ae2b666115cd9ebb`  
		Last Modified: Wed, 17 Jun 2026 22:39:31 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:380472683aa29e3aa875760c33a0ae6683abea6d61ff7fdb3ca86ce56d1d542f`  
		Last Modified: Wed, 17 Jun 2026 22:39:32 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091478b1d70939e2c9b41e3fca6d7a9704cf1d843aff7cf7629979667c96fef9`  
		Last Modified: Wed, 17 Jun 2026 22:39:32 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:e24fb005457cae955fcd07d8a4cce5439ab63b6ebb59254c4f0155cc1b9fea5c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef27cd622da839b9c631506886ffb7c7837ae56742dfe7867e6d71b0c37d4619`

```dockerfile
```

-	Layers:
	-	`sha256:f16248f6a507542fa047a9821787135be28fb4239b95ca0ac043bbe8b5ab49ec`  
		Last Modified: Wed, 17 Jun 2026 22:39:31 GMT  
		Size: 2.8 MB (2841150 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:219ba3ade633ca21a7c6a9d8ed0f71025220fb0368845800e5e2841a83d2c7bf`  
		Last Modified: Wed, 17 Jun 2026 22:39:31 GMT  
		Size: 34.0 KB (34039 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:5d4cd3598efcf9442498e6270cf10174bced9b57f961c69284b98c9a06cee881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61398641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd83541abc246e62e0ceb81446204983f5dbbafeb7f53af4d5e0da828b37648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 22:32:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:32:49 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:32:49 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 22:32:49 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:32:49 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 22:32:49 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:32:49 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:32:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:32:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:32:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:32:49 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:32:49 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:32:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60af9b45fe503364ef559a5b6296b2e189beb1bf9f6f176abd003358fdda3ef3`  
		Last Modified: Wed, 17 Jun 2026 22:32:59 GMT  
		Size: 31.2 MB (31245517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60050dfc039c42ed2c491064d7152ab668d4547b447d06c8bfd9a73178e5e8a0`  
		Last Modified: Wed, 17 Jun 2026 22:32:58 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b74f5c7f9b1bbea7de3d7aa9e4ad4ca0ed0a87fbe7556b6a89cbb83a72ef6592`  
		Last Modified: Wed, 17 Jun 2026 22:32:58 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35bbfc5d98274353e623ba517257f7c3e35b4baddd2c1ffff34bf775fc969edb`  
		Last Modified: Wed, 17 Jun 2026 22:32:58 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6fbcade2b55ce26d8c94c0c462f9da6b36f4e403fbd7fb9fb6095802c5e8357`  
		Last Modified: Wed, 17 Jun 2026 22:32:59 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaafd8db6b68dd0a917d0bd294b2b13a740cee121d340d616a24400ea31abd9c`  
		Last Modified: Wed, 17 Jun 2026 22:32:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:1813a27aed9cb9c833e819335166a37a230b720c172ed983c8c4e64299434f2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2850796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cc94677aa80066a994371bb54a37f243de39c5b4f3d2d4e844f5824d7162fac`

```dockerfile
```

-	Layers:
	-	`sha256:46376121305e7af6127382c984c046ac0f82404a38bbc824917f73ba25c407e1`  
		Last Modified: Wed, 17 Jun 2026 22:32:58 GMT  
		Size: 2.8 MB (2816725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea340144c8a733772fb20746b305b0a39b94b34ed027ce4e23ad92e54dbfca15`  
		Last Modified: Wed, 17 Jun 2026 22:32:58 GMT  
		Size: 34.1 KB (34071 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; 386

```console
$ docker pull nginx@sha256:953f300286f8bfe396f0da1aaf88944710b73be3e7a5d14072c0254a39db8575
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63457104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9513138fe87914f4cbb681c6c52d7d6f7b3bf3fdd045cede9183a93a6b65a77`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 22:35:22 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 22:35:22 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 22:35:22 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 22:35:22 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:35:22 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 22:35:22 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:35:22 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 22:35:22 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:35:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 22:35:22 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:35:22 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:35:22 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:35:22 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 22:35:22 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 22:35:22 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 22:35:22 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 22:35:22 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f157b8aac097d97be60c140337da8eb6c29d9f0ca4b63572a13c7665f3dddf0a`  
		Last Modified: Wed, 17 Jun 2026 22:35:32 GMT  
		Size: 32.2 MB (32151305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82605bbc8b19ce5d559fe5bbf0d6cd5725fdef251c924976935e704b4f5e05a9`  
		Last Modified: Wed, 17 Jun 2026 22:35:31 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e80654f0205dc44e138c533e77e0fc03afa1df1e8efce72a99d1293ee695158b`  
		Last Modified: Wed, 17 Jun 2026 22:35:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b55eedf95f535cbaac74f36d9de48f67a02a275be51be6a85a526aef179c106`  
		Last Modified: Wed, 17 Jun 2026 22:35:31 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72c5eb5174309d0d716097548040137534c13551a54a6346370785156e7d5e70`  
		Last Modified: Wed, 17 Jun 2026 22:35:32 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5e905a928d06f2b60943ee76aa4ead9533396167164e052ef4d6969d773da25`  
		Last Modified: Wed, 17 Jun 2026 22:35:32 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:53f09e683f308096d9f65540b87190c0278c574ef3a227fa40a91bd21a1e9236
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2870054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d266da75ab04b159a6787828e99c8f8633f005b0809ab67ba5f136e5fc5d9379`

```dockerfile
```

-	Layers:
	-	`sha256:6b6bfc926d7748d3d910b22042f3eee878aa94cc8ec8e270d6d0d6e0beb7e50a`  
		Last Modified: Wed, 17 Jun 2026 22:35:32 GMT  
		Size: 2.8 MB (2836153 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03b015603cec2eb83e846639cb0f8d6f88e97479722dc5d7bd739b0b9bb8cd2a`  
		Last Modified: Wed, 17 Jun 2026 22:35:31 GMT  
		Size: 33.9 KB (33901 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:4af9ea368c602e70f7adfb2d36ddacd2fe4d0cbacd3d86b8594254872907c5bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67212247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e47c0b0524773bbf4ef8280f7e3ba287e04b98e0dc99505427a76f45c8f1b9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 23:38:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 23:38:26 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 23:38:26 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 23:38:26 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 23:38:26 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 23:38:26 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 23:38:26 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 23:38:26 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:38:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 23:38:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:38:27 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:38:28 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:38:28 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:38:28 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 23:38:28 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 23:38:28 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 23:38:28 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cd81c32e08f21a2aeca0d0223dca5b73d52ab6563c9bee2f7ab629eab6cfc8`  
		Last Modified: Wed, 17 Jun 2026 23:38:46 GMT  
		Size: 33.6 MB (33601303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45411783e19644a15c1f94630ed8e8992303ed3be579f828ac9ca328443b04c`  
		Last Modified: Wed, 17 Jun 2026 23:38:45 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65e363b892564aa28470cc42738969a1d523698a56ad7a9f33f8c094f64a1ffe`  
		Last Modified: Wed, 17 Jun 2026 23:38:45 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88127d8cb9449d372b6a2e29f3ec4e07771f76a3f5e5126b01aef2af103662f`  
		Last Modified: Wed, 17 Jun 2026 23:38:45 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65614be3125b5c47574ef0b6fe7c1bbbcc7b0699d511226b64dfd77587da313f`  
		Last Modified: Wed, 17 Jun 2026 23:38:46 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10eef815d24c0cebd85e62471c62c9ea58be35037154620dc027157a8670d9ab`  
		Last Modified: Wed, 17 Jun 2026 23:38:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:30e20c320a2a8d872fff2e9cf6aeb3c40914d3df494e2a91a8ba03b6143d2c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877801 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c1eb77de87f340d32ddc30e5222109f93e527d6fe8f64d7c5f014586d44d353`

```dockerfile
```

-	Layers:
	-	`sha256:3bdd440a77947f7f6a597f2b0ecc6f02a1aa6f14780b33dc36738fb9a5fa55dd`  
		Last Modified: Wed, 17 Jun 2026 23:38:46 GMT  
		Size: 2.8 MB (2843803 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b971f9da90633baffe99da8350576d1a868f6a74f8cd4a47e2611fe4305e8ff1`  
		Last Modified: Wed, 17 Jun 2026 23:38:45 GMT  
		Size: 34.0 KB (33998 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:7dc6ccb4284de735848e4eb508f1a959d4a9fc1aaaf6d2d12da73aee8a56bd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57756063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9fcd333cfc67fd12359413b24d93c49e28be296b21ff05211a386c2d64c7079`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Fri, 12 Jun 2026 06:12:42 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 12 Jun 2026 06:12:42 GMT
ENV NGINX_VERSION=1.30.2
# Fri, 12 Jun 2026 06:12:42 GMT
ENV NJS_VERSION=0.9.9
# Fri, 12 Jun 2026 06:12:42 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 12 Jun 2026 06:12:42 GMT
ENV ACME_VERSION=0.4.1
# Fri, 12 Jun 2026 06:12:42 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 12 Jun 2026 06:12:42 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 12 Jun 2026 06:12:42 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="60789259bfab36b1669a414881a9d002fd246d6b"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="9282a0265c921af3e2d5760cbdc06aae65e6efb145ed266fe02102326174a9e9405f6492979372556c14e2f4f8cf66a48c338d054d0ece375a1c41f343f244cc *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 12 Jun 2026 06:12:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 12 Jun 2026 06:12:42 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 12 Jun 2026 06:12:42 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 12 Jun 2026 06:12:42 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 12 Jun 2026 06:12:43 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 12 Jun 2026 06:12:43 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 12 Jun 2026 06:12:43 GMT
EXPOSE map[80/tcp:{}]
# Fri, 12 Jun 2026 06:12:43 GMT
STOPSIGNAL SIGQUIT
# Fri, 12 Jun 2026 06:12:43 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c976de384764557649768e1a26a15b1f363444f47bc333422f0c72fa6b32e4c0`  
		Last Modified: Fri, 12 Jun 2026 06:14:15 GMT  
		Size: 29.5 MB (29469145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6459c6a4dc2206cd0655aac0a2ac4cf7285cc255f50e16a42460361b7488ca9a`  
		Last Modified: Fri, 12 Jun 2026 06:14:10 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0ff802dde235c074885ebd8822498dba704cc67369e0308d7c649020ceef796`  
		Last Modified: Fri, 12 Jun 2026 06:14:10 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76a9ce656f09bbbd8d5d12eaea24e818ad4dee6833edd1eecbb3e197b34a64f5`  
		Last Modified: Fri, 12 Jun 2026 06:14:10 GMT  
		Size: 408.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c7c4fde4d52c8a18247293209d587a7f5deab2d2a09c30b029f1ac9fd6d8304`  
		Last Modified: Fri, 12 Jun 2026 06:14:11 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a61b06160f6b8f0fc51204dd8de919094c6e974d86a2026739853c148df1a5c4`  
		Last Modified: Fri, 12 Jun 2026 06:14:12 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:fd263c0ce8434685164aed628fcd819a4ab305f5ecc4643f9b6d1d3fbbfa8b62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867609 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a165be413ffee3447cc02aa2d9e9fb7ea31b166f32885885d4eeb65f56e356a`

```dockerfile
```

-	Layers:
	-	`sha256:ed2f1b0cad70a415a3f985cb77fac7548b1448a4e7d2f3590ffdeb751a9ddbbb`  
		Last Modified: Fri, 12 Jun 2026 06:14:11 GMT  
		Size: 2.8 MB (2833590 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b54560b24a9700481419c961eefc5149ce3f8a31a4bee0908e43fd912e37379`  
		Last Modified: Fri, 12 Jun 2026 06:14:10 GMT  
		Size: 34.0 KB (34019 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:693318e31b17b5d2837f4f27787aa83029a736e468433c9e411ec4c24fc1a68f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60639806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b362eac4b2b87b994296e6caa03674597264347d6a3d93db3d2ca13acc0162b4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Wed, 17 Jun 2026 23:08:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 17 Jun 2026 23:08:49 GMT
ENV NGINX_VERSION=1.30.3
# Wed, 17 Jun 2026 23:08:49 GMT
ENV NJS_VERSION=0.9.9
# Wed, 17 Jun 2026 23:08:49 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 17 Jun 2026 23:08:49 GMT
ENV ACME_VERSION=0.4.1
# Wed, 17 Jun 2026 23:08:49 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 23:08:49 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 17 Jun 2026 23:08:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e602521342632b9cd61ff29049864eb5e233dea98918f1a4d842c4fb8304af1f916a9630e9cd00236366f713a011ed6b05e068ebcc136d3d820af0c31f932a71 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:08:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 17 Jun 2026 23:08:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:08:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:08:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:08:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 17 Jun 2026 23:08:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 17 Jun 2026 23:08:50 GMT
EXPOSE map[80/tcp:{}]
# Wed, 17 Jun 2026 23:08:50 GMT
STOPSIGNAL SIGQUIT
# Wed, 17 Jun 2026 23:08:50 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47f150c758f829f843464425c81135dccfd51c029feec8ecd2c858f973190e7d`  
		Last Modified: Wed, 17 Jun 2026 23:09:05 GMT  
		Size: 30.8 MB (30783848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:209bd5a5400969c895c6cd0fb3cebe1b1e0ee67d84896c679cbd584a2b4994e5`  
		Last Modified: Wed, 17 Jun 2026 23:09:05 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acb8485b98289846e598d985029704d97ee0d0be77f8e7fce629c3f3e5951888`  
		Last Modified: Wed, 17 Jun 2026 23:09:04 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97998f37ab0cea1c1fdd1ae29aec51b0e0f05373064db5a34900d7534d091701`  
		Last Modified: Wed, 17 Jun 2026 23:09:04 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbc33e39bb0081cd27c949cd53717c4daf7e489d83b339e3f8713fb7b5c02587`  
		Last Modified: Wed, 17 Jun 2026 23:09:05 GMT  
		Size: 1.2 KB (1214 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbe9328a03836bd03e5db55ff9681575c50e5a388ac34324e93c66ef488bcd1`  
		Last Modified: Wed, 17 Jun 2026 23:09:05 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:fbc83da814a89500b79bdc583fb444a7de3064bcaa4d8e8f096ddc260d246d7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2783526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21d9121af2f6588115fc0ba49319b06d7dc45e020acb68cd877efba756b3153c`

```dockerfile
```

-	Layers:
	-	`sha256:374b8d948f33612830bdb4bfa2eb0cf55802632224c5b3c433225c857a73c7dd`  
		Last Modified: Wed, 17 Jun 2026 23:09:04 GMT  
		Size: 2.7 MB (2749583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a145a259be67ebe4a9d6327486a22d23c9962879c0c4ddff3fa7378a64663ce6`  
		Last Modified: Wed, 17 Jun 2026 23:09:04 GMT  
		Size: 33.9 KB (33943 bytes)  
		MIME: application/vnd.in-toto+json
