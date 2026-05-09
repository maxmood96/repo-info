## `nginx:latest`

```console
$ docker pull nginx@sha256:1881968aff6f7cdcc4b888c00a11f4ce241ad7ec957e0cb4a9e19e93a3ff87ea
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

### `nginx:latest` - linux; amd64

```console
$ docker pull nginx@sha256:ab15d428b6a7121511a38221591a41f835933ac16f996fafd102d128a0fa20f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62942486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5dfe511714e1fa9a9d1074193a6cc7fa0feab5d680be166336817a5fb57f4cbd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:22:39 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:22:39 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:22:39 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:39 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:22:39 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:39 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:39 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:22:39 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:22:39 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:22:39 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38a7e44929f3a02caf5d606403b9c7f843cf5fd963a30bd77d9a4deea44cc4e0`  
		Last Modified: Fri, 08 May 2026 19:22:50 GMT  
		Size: 33.2 MB (33157664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9f32fdbd611e27f05fbb3d972c3cbd1d9ce01dcf9743667b551f37a12b9d7a`  
		Last Modified: Fri, 08 May 2026 19:22:48 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382a36159731b6c4f15992b4542ad824d7a1d3dee549d696ec8d4af8f0718466`  
		Last Modified: Fri, 08 May 2026 19:22:48 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20d41cd6829d6a76246d76ad30405271259064cd1465c2f49b8f0f03a63675f5`  
		Last Modified: Fri, 08 May 2026 19:22:49 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83742381311ab223ac476c81482f79c2fd5f8cade0fdd7c3ee92574649e9ace7`  
		Last Modified: Fri, 08 May 2026 19:22:49 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e9b53b630dedfac569c0b3484f367dd8bdaa437b2dcff5c453b742fcba600cf`  
		Last Modified: Fri, 08 May 2026 19:22:50 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:bf34a2efe16261f3df780ef1aaa3d34d2e2f85d7257b3ffc1b20f78de52a41f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:227a3c065451c87289fecd47d877c748ac4b18e72a93ee048b2510b7a1af14a4`

```dockerfile
```

-	Layers:
	-	`sha256:46ca9676efb5324d0e9202a7d8039ab077152bfb09643c57ae03ada397aef054`  
		Last Modified: Fri, 08 May 2026 19:22:49 GMT  
		Size: 2.8 MB (2817297 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a543ead0f2dd25d2f358731e00896251953fdd7696fea1bee0e7d82ac7e9e4`  
		Last Modified: Fri, 08 May 2026 19:22:48 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm variant v5

```console
$ docker pull nginx@sha256:ffc53e3b7885c0c44499b6e3635d93a32ca984cabd27b5126f08b7fdc25dc42d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54152350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9757aa3eb5a01cdf306725ae767bb9c5323b06c08d18e32875c6b8c5a86a78`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 20:35:51 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 20:35:51 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 20:35:51 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:51 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 20:35:51 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:51 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:51 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:35:51 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:35:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 20:35:51 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:248401f980342939fee4bdb4ca9fb00391cc1aa9f64bd3563b47b38ad3f78c5b`  
		Last Modified: Fri, 08 May 2026 20:36:01 GMT  
		Size: 26.2 MB (26199553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdc941638861d65831d90b9caf1b2c9d1315947ff2e923fbe375ac4184521135`  
		Last Modified: Fri, 08 May 2026 20:35:59 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ec5ae31c39e063380c2963694757fa05e0f3dace00508ff27ef9c00b918901a`  
		Last Modified: Fri, 08 May 2026 20:36:00 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77d671da6a4cdd2e80fc9fd343e2cd233f549217050b939eb93fcb5209774a09`  
		Last Modified: Fri, 08 May 2026 20:36:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3098863e501eb5764fa816da952454ce0e1102200cf503439e13575466e405d8`  
		Last Modified: Fri, 08 May 2026 20:36:01 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74e03ff89f4d7bd993ae573f1f4226d1ec56e334400d63bc6d2569506736eb4c`  
		Last Modified: Fri, 08 May 2026 20:36:01 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:8d604642559c01a032a83a2a0b9844e6f6e5c03c31e5ecac5298e89e55bd8eb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2878721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b314ee6d98ff6ed9b7820b69983a0f8018c988255fc4cfdfa629b791ea1695e6`

```dockerfile
```

-	Layers:
	-	`sha256:8428c1d256a2ac0130304766214f45b0c5b9f3c322ae218405ec44a0c0d639be`  
		Last Modified: Fri, 08 May 2026 20:36:00 GMT  
		Size: 2.8 MB (2843437 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0977e99a8295774f3ead31f5886fd1ecb21c47b50f5dd3946125bd1f56fef7ee`  
		Last Modified: Fri, 08 May 2026 20:36:00 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm variant v7

```console
$ docker pull nginx@sha256:cb4a8f310edfae454ff42daeb7e4e855ea4d97dee92cc74e7581860ec7e73d38
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52361263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c07445297aefcd8ea90d108e431ee1333a1f81c282ead7a7cb2fb02759ca4b10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:24:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:24:26 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:24:26 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:24:26 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:26 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:24:26 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:26 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:26 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:26 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:26 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:24:26 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:24:26 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d0c12dea6b68e914ece1edc0cb20c87b4489c8a716f3e354e2c95696c5631aa`  
		Last Modified: Fri, 08 May 2026 19:24:35 GMT  
		Size: 26.1 MB (26141751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e814b586bf73d67e3579baf6c1080fdb4f8000ea859be552ea90c5831fed0ef`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6651b6ff0d24cd91e484161816d722d9ef78473d20aa6d0e0a04f2562e138afe`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc0c33d585f0caca673715dcc76092bf0b01c98a01ab46e3db5b7d1f0bdcc37`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d490978ee28bd10e13b66791c5b29fd1c656598bca3bc5e9b9b356b9788638f0`  
		Last Modified: Fri, 08 May 2026 19:24:35 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b383a10d7f7c8a8cfb7f750cea6ae2b04c9a148427193ed52ee51b24574cd8cd`  
		Last Modified: Fri, 08 May 2026 19:24:35 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:cf946a95afdc479c45d9f67c2f466dd10d490cc4c5432dfb4ae4680a34954091
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f7cfe099aab1fcaa1c4dafaccde1896ae6849be0f670b8c358199998f46ee89`

```dockerfile
```

-	Layers:
	-	`sha256:5658a4775846f0144dbe5f3f08495e291caf5091112323d4c4ba232fab30cf11`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 2.8 MB (2842182 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f30411dd175990e283c25505c0855c9490d199f69ec07779489672070642dd6`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 35.3 KB (35283 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:c5c2b964a499822699fdf5e520bf8a3c2cc6434f8caac07a2028d7f3023b9972
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61288689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8524ce6c9242ecdadb2974f0924ce4dd02f04d46915d5a0076eeccc0208cd6f8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:36 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:21:36 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:21:36 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:21:36 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:36 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:21:36 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:36 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:36 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:36 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:21:36 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:21:36 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cbb36225b641a6965b680bcd401a43615e52a42e93908d0faf2388cb088d143`  
		Last Modified: Fri, 08 May 2026 19:21:46 GMT  
		Size: 31.1 MB (31140455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7233902120245103cf1634f36441eb74882a602b9c7934f85696d7896c8802aa`  
		Last Modified: Fri, 08 May 2026 19:21:45 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e26c83bf44f3bf345dc97aed90b8a0cd2111861f2c76c35c29985c26a0b6483`  
		Last Modified: Fri, 08 May 2026 19:21:45 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d472f762a89436d52a3327293fdc6b426321be07ffee13227faac78b82b466`  
		Last Modified: Fri, 08 May 2026 19:21:45 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b08d37673839087af78b752a824ef4f692acd5190a9eb34b91b8f6e4875d9c4f`  
		Last Modified: Fri, 08 May 2026 19:21:46 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d207385a9f9125e7d6d972d71854facba065523c9fe2b8d350264acb05e5a03`  
		Last Modified: Fri, 08 May 2026 19:21:47 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:ed5a410d4e00c9c70c0f7e76b9e27d32b4db688d581b1797fded4c543bb19041
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853113 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f649497d98de54d13ed07674dd43cf1d37f8bde9e1850eec2c2b257edd955cc`

```dockerfile
```

-	Layers:
	-	`sha256:cd4a1db27322ed4da8313232e09e5f9d2e776aea8ab773f24c9b666aae052609`  
		Last Modified: Fri, 08 May 2026 19:21:46 GMT  
		Size: 2.8 MB (2817781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c776f4dc3e8d576ff5616f74e52b993f9d62e0d0ba9ad61a7d2e0024732909b7`  
		Last Modified: Fri, 08 May 2026 19:21:45 GMT  
		Size: 35.3 KB (35332 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; 386

```console
$ docker pull nginx@sha256:b3e4fcd73ae4790c7b1a3fa657775334885ec2ba6b846363f377e44ae1fa9569
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63327172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2996b485a51d06b6d7ddaec138c39b5736acd28db389cb61ca034bf3fe3286fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:24:17 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:24:17 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:24:17 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:24:17 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:17 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:24:17 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:17 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:17 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:24:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:24:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:24:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d05dbf9207fd2bf33fd8ac273953d1ab6e047dfb2c0b578bec2bbeec2793c307`  
		Last Modified: Fri, 08 May 2026 19:24:28 GMT  
		Size: 32.0 MB (32026180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352c41de7e8b07879566636ec7384dcbb0e4ad6a5085b025852f925ab7e3bae`  
		Last Modified: Fri, 08 May 2026 19:24:26 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00b9fb5b9b9ee5f715cbc92c29cc56af391476544fa78f7c99314a5c40c77db6`  
		Last Modified: Fri, 08 May 2026 19:24:27 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31c261b893d72e4fd5d7036cfd06e82b2cd81c32cd7782c3f51908896301ced5`  
		Last Modified: Fri, 08 May 2026 19:24:27 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:381f65747989b45bd5d8b02dbb48a37dd2e6cd5f5accd1b47231ba4092532847`  
		Last Modified: Fri, 08 May 2026 19:24:28 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:978ed3b36cfb1d4f51d4a4f7db3b91eb75cb2dfba5657f30d5968aac8225e18c`  
		Last Modified: Fri, 08 May 2026 19:24:28 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:29f8792d7768eb6c447cbcc1833da24cbe895315aaf6c2349db3e52d41afb04f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c66e9c8d29ae1da19d2375aa91ed3e2a3e26a847d2e6aef04567d71d39fa58`

```dockerfile
```

-	Layers:
	-	`sha256:ef2c7f46c7cba075098ae42b2c10fc0fed6091651e7b78997fb466ba05c19780`  
		Last Modified: Fri, 08 May 2026 19:24:27 GMT  
		Size: 2.8 MB (2837133 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a3e5830de27b23f8afe9d2ed2b1907ba24f28e2ea5fb7f6d9225a7fe85e03b6`  
		Last Modified: Fri, 08 May 2026 19:24:26 GMT  
		Size: 35.1 KB (35094 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; ppc64le

```console
$ docker pull nginx@sha256:aa5111c369c4db3c2337046adacc924f3bed87f5d9b2932fb84ee2e955d424ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67086000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fd7f690e7f5715b5e8db41a87064a27f2d21f191ac5db9b91e45c4e05f46391`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:49:16 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 20:49:16 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 20:49:16 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 20:49:16 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 20:49:16 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 20:49:16 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:49:16 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:49:16 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:49:17 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 20:49:17 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:49:17 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:49:17 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:49:17 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:49:17 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:49:17 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:49:17 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 20:49:17 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a639dc5bce02840e364ae35b10a41573d329c7d64c25f1b16a7cb0bde1e8a273`  
		Last Modified: Fri, 08 May 2026 20:49:37 GMT  
		Size: 33.5 MB (33483311 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c79ff3523a7ca66d59e38f536975d2d6e04d0ede24d35c8cb3166fb3a89fa36`  
		Last Modified: Fri, 08 May 2026 20:49:36 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb6e2a18fc0903f5bcf95fcae8ed27df272f773d2724741bbc91ef82ef50fce`  
		Last Modified: Fri, 08 May 2026 20:49:36 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90bfeee7648e6e67cbdac1c3fea5ebb4c865cc26cfddf48f0a4d8ae1416dd97f`  
		Last Modified: Fri, 08 May 2026 20:49:36 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62e24beb92ab0e377ef49c75769c333246514d6566e0cb1925855e89786d1d61`  
		Last Modified: Fri, 08 May 2026 20:49:37 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:672e17404f6113f30a82d3cf1b9a39f594ec2c57bfbbc2a0451accee42a094d4`  
		Last Modified: Fri, 08 May 2026 20:49:37 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:f179eef9565391f0b072f7e8a8b0d63d27421d175436bf54c47e5af9bc6589e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a036f8f938c25ed3af979c7aa8f594e90952c80377760893b7218e8ad5855ef`

```dockerfile
```

-	Layers:
	-	`sha256:a803b00e9de6ecf5093b5d2666659418635c4afb8b1cd167100add6c81f8e866`  
		Last Modified: Fri, 08 May 2026 20:49:36 GMT  
		Size: 2.8 MB (2844827 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e19e25942d3ed5c10826ddd4e1b3c517507adc8127169a8d0d64da72eeb5cd72`  
		Last Modified: Fri, 08 May 2026 20:49:36 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; riscv64

```console
$ docker pull nginx@sha256:6b6f696d2fc48167cbd86e6c334eb20b71f3b00949829e924362e9bcc41b8484
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57652697 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0133a09354a92ebf3067cfee510cf0f8c5266a7051fd046037090a081ddfdf49`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Sat, 09 May 2026 19:08:15 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 09 May 2026 19:08:15 GMT
ENV NGINX_VERSION=1.29.8
# Sat, 09 May 2026 19:08:15 GMT
ENV NJS_VERSION=0.9.6
# Sat, 09 May 2026 19:08:15 GMT
ENV NJS_RELEASE=1~trixie
# Sat, 09 May 2026 19:08:15 GMT
ENV ACME_VERSION=0.3.1
# Sat, 09 May 2026 19:08:15 GMT
ENV PKG_RELEASE=1~trixie
# Sat, 09 May 2026 19:08:15 GMT
ENV DYNPKG_RELEASE=1~trixie
# Sat, 09 May 2026 19:08:15 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Sat, 09 May 2026 19:08:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 09 May 2026 19:08:15 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Sat, 09 May 2026 19:08:16 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Sat, 09 May 2026 19:08:16 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Sat, 09 May 2026 19:08:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Sat, 09 May 2026 19:08:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 09 May 2026 19:08:16 GMT
EXPOSE map[80/tcp:{}]
# Sat, 09 May 2026 19:08:16 GMT
STOPSIGNAL SIGQUIT
# Sat, 09 May 2026 19:08:16 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44264177fea2e5b609c2f33b5bc1bfbf8e8f8bedbfaf53ab2d99ebddb2808f0d`  
		Last Modified: Sat, 09 May 2026 19:09:46 GMT  
		Size: 29.4 MB (29367856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c290b95cfdd1154decb2265cb3f15eeaed53ea0257f5cbf18c2d3f25919502d5`  
		Last Modified: Sat, 09 May 2026 19:09:41 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c96741f88e9fdc22ba21ff5d640c7e14cd22f4b86767428532a9884e7ca63772`  
		Last Modified: Sat, 09 May 2026 19:09:41 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:606064323df09361bf37226ea12f14f00ce83862243c020e30fe189df992b690`  
		Last Modified: Sat, 09 May 2026 19:09:41 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd72dd9c366d8d5becca0e69a3f260c4dd141b6fcf9c599a755270d840d4ece7`  
		Last Modified: Sat, 09 May 2026 19:09:43 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f50a7aa1ea92bd8a02bdb7ffccccb52a2ce301aeefd0ce8ed26b75178d2f9a0`  
		Last Modified: Sat, 09 May 2026 19:09:43 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:a5f64f4c91e1cdec5cd2510764ba7310dc58206518cfe87bd3ca9b3e4d6ef9de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:660b6858ef51b783d48289aca493cb56a7ac6f1a2e6a9725d56df2e7f7d97a2a`

```dockerfile
```

-	Layers:
	-	`sha256:cca23f7b9299e596380107db76fc00d5891310bf346dc1ac762bdb4575eae850`  
		Last Modified: Sat, 09 May 2026 19:09:42 GMT  
		Size: 2.8 MB (2834614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06ea70dbefbc932aaead10a4d8ee353199fa6afba64acf6cd75ac7bede5c9693`  
		Last Modified: Sat, 09 May 2026 19:09:41 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:latest` - linux; s390x

```console
$ docker pull nginx@sha256:525129cffca205d9d4bbd41ce13bcbb47defb59b289d1972fa0589ec0cfe7515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60498673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ef4ede20cc7ecaa3ce46962a5a7baa1b0ead79f55c027a48563b09569b01e08`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:26:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:26:49 GMT
ENV NGINX_VERSION=1.29.8
# Fri, 08 May 2026 19:26:49 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:26:49 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:26:49 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:26:49 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:26:49 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:26:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7074c3ba1ece708140afd0220b16df77651fbb56cc012e901bc1c4a80531872b7a58ad97a28357646575ce625e94a0540796c045f95d33e40e6d3874ce7b3d79 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:26:50 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:26:50 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:26:50 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:26:50 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0b03df5ff49f009a8cabfddb18af44a2f4694cd15719407eec4c9c9bf539b6`  
		Last Modified: Fri, 08 May 2026 19:27:17 GMT  
		Size: 30.7 MB (30653718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb7780fd36b86f2fd663827127e327928c9816bf5738fd567408b97bae1951cf`  
		Last Modified: Fri, 08 May 2026 19:27:15 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21490a4124568a5aa7f84106ba4f0c89808702ff1607545461f3de38df2ebed3`  
		Last Modified: Fri, 08 May 2026 19:27:15 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91d51ae9c5e3f0102859f06fed00738d708a295b93f1c7df39d8098e81e469af`  
		Last Modified: Fri, 08 May 2026 19:27:16 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa3514432aae0926679a5f47a633a805c695af27cbb50bd07a16055576034b9e`  
		Last Modified: Fri, 08 May 2026 19:27:17 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d30b4517fdedc22ec08d4e7b57dc3bd665d01cd3ce777dd391a1b3ebe77d0d5c`  
		Last Modified: Fri, 08 May 2026 19:27:17 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:latest` - unknown; unknown

```console
$ docker pull nginx@sha256:72bd423eb7f162961d1b0f42c6980fbc696fe69e715854411298b9b03c6d5495
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42d1db6d4a537353134bd4b17f894290b9c2d2b3bebb61c8109f647d68a55503`

```dockerfile
```

-	Layers:
	-	`sha256:409ea221343119c594eeb5c5c726789e9be0dad33cc4c4d87720e2ac28554d26`  
		Last Modified: Fri, 08 May 2026 19:27:16 GMT  
		Size: 2.8 MB (2750583 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2c12eff082b799e4e7bf6136a77856c4ec9e07e5aa718cca3fb5e6d295ebe33c`  
		Last Modified: Fri, 08 May 2026 19:27:15 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json
