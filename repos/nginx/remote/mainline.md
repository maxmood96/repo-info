## `nginx:mainline`

```console
$ docker pull nginx@sha256:94ef2bdc0b32e45530840de5e08a5856429322546a45d6cea21609890af5b635
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

### `nginx:mainline` - linux; amd64

```console
$ docker pull nginx@sha256:4a2d27f57e72adbc1e1cfed8db6cbdef22c080e058565f92647f7aad258292f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.1 MB (63104350 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:936fef290c8f5ba8f81fb245148be818bef3f64badd90787c817ffde939cd6a5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:30 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 11 Jun 2026 00:23:30 GMT
ENV NGINX_VERSION=1.31.1
# Thu, 11 Jun 2026 00:23:30 GMT
ENV NJS_VERSION=0.9.9
# Thu, 11 Jun 2026 00:23:30 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:23:30 GMT
ENV ACME_VERSION=0.4.1
# Thu, 11 Jun 2026 00:23:30 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:23:30 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:23:30 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 00:23:30 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:30 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:30 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:30 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:30 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:23:30 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:23:30 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:72c03230f1363a3fb61d2f98504cf168bad3fe22f511ad2005dc021515d7ce97`  
		Last Modified: Wed, 10 Jun 2026 23:40:25 GMT  
		Size: 29.8 MB (29785415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4dcde3aeeedc4744f6c3a6c1f6d51eb75e01955bbef0480617fb91c0522f211`  
		Last Modified: Thu, 11 Jun 2026 00:23:40 GMT  
		Size: 33.3 MB (33314329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5a7565de4cfb2ece2cfa07cf5c08da0ef0d447f9eca7e386bb504bd279e6407`  
		Last Modified: Thu, 11 Jun 2026 00:23:39 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57b3fbf43092480ec04b52f6d3d94b4b0e016aa9792bde6d363e8aa956030bf5`  
		Last Modified: Thu, 11 Jun 2026 00:23:39 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80fa08b690ad61a19ed8ce2f58d50efcd25036b4e0619dec599e9bbb7dc0101e`  
		Last Modified: Thu, 11 Jun 2026 00:23:39 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41c9f6f909405b416a21da29f1f8b453d243d27a61fe7d06c202f273c7b25669`  
		Last Modified: Thu, 11 Jun 2026 00:23:41 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6376488be516899e64d9cfac0e1a6a931e5e7487aaa820047a3e30a9a2e7c877`  
		Last Modified: Thu, 11 Jun 2026 00:23:41 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:3c44ebb00f85ccf90d28d6e235a0bdaad54181b655adf317a543259e907b6095
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9332214b6fbd27ce6097c4d9ce6fe6d81387203de8a660d8d9eb9af109f679b7`

```dockerfile
```

-	Layers:
	-	`sha256:ce322055c0f53443969c1a688f2cd7dee523313b1ae0c8dbfdd524f8d8ab20d6`  
		Last Modified: Thu, 11 Jun 2026 00:23:40 GMT  
		Size: 2.8 MB (2817483 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9bebb266cee4ee127f2f7d4a1b6feb2fe8be357d68a8d060e9e22f182d1e032c`  
		Last Modified: Thu, 11 Jun 2026 00:23:39 GMT  
		Size: 35.2 KB (35177 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v5

```console
$ docker pull nginx@sha256:c03e7dc5f0976f810d167e8998fa192a0efdb2e0c348189da6949d2ebe3d55a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.3 MB (54262253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b8a486adbdc413e2cb8c9990e461ad4652bc0db9fe7204734d61dbc5978de69`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:29:33 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 11 Jun 2026 00:29:33 GMT
ENV NGINX_VERSION=1.31.1
# Thu, 11 Jun 2026 00:29:33 GMT
ENV NJS_VERSION=0.9.9
# Thu, 11 Jun 2026 00:29:33 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:29:33 GMT
ENV ACME_VERSION=0.4.1
# Thu, 11 Jun 2026 00:29:33 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:29:33 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:29:33 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:33 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 00:29:33 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:33 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:33 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:33 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:33 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:29:33 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:29:33 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:29:33 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efcc21b88a9a0a138bc94b696566f79b4ec54f3a5491e66783108b7136858015`  
		Last Modified: Thu, 11 Jun 2026 00:29:42 GMT  
		Size: 26.3 MB (26298450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c25b5f504af89204fec84bfd4ba609a2d7e0dd1b5d3eb34c75a2d656d34161`  
		Last Modified: Thu, 11 Jun 2026 00:29:41 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f2facc64fcc296d278c179865738d107f0af270f720be27d016d61f5fd72eed`  
		Last Modified: Thu, 11 Jun 2026 00:29:41 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94acefcf10807393a201279c417dec82221720fac2824d179a757cbeef68074f`  
		Last Modified: Thu, 11 Jun 2026 00:29:42 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3705fb7bd5780c8dedbe51a38ec7dcb1f340fa156845696c0320b76bcbd5530a`  
		Last Modified: Thu, 11 Jun 2026 00:29:43 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de64d986594ef335ba586a7a0efd3aa99c207a8e05003d0f97289247dda8116d`  
		Last Modified: Thu, 11 Jun 2026 00:29:43 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:66fbe253060c7ab82f13dbc9c86d86300b24986dc788302f216a7d686e118f51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2878926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6aed565d34a575323875a335e0f5db86a1b3ef6c7fb04f8d22b0575fc67f5969`

```dockerfile
```

-	Layers:
	-	`sha256:67faa2791c6b584942ad79eae51b634a79cefde6dde123a01edbf75ed6749c9b`  
		Last Modified: Thu, 11 Jun 2026 00:29:42 GMT  
		Size: 2.8 MB (2843623 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffb4a2147790cca55ac753037244617589f63683bbbbdeb9fad418226bab8485`  
		Last Modified: Thu, 11 Jun 2026 00:29:41 GMT  
		Size: 35.3 KB (35303 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v7

```console
$ docker pull nginx@sha256:fad9e81da1016e799ca548536cb817d7280a69f50fb4c3a180b88024c41ccff8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52461384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cffd77756f28fd93375c32985f1e192206d7c978eda3678dce7041742fdbcd2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:30:47 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 11 Jun 2026 00:30:47 GMT
ENV NGINX_VERSION=1.31.1
# Thu, 11 Jun 2026 00:30:47 GMT
ENV NJS_VERSION=0.9.9
# Thu, 11 Jun 2026 00:30:47 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:30:47 GMT
ENV ACME_VERSION=0.4.1
# Thu, 11 Jun 2026 00:30:47 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:30:47 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:30:47 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:30:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 00:30:47 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:30:47 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:30:47 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:30:47 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:30:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:30:47 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:30:47 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:30:47 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f92e1d249fe32e375ea1ba60e87767af4c9e70c8874b4be564acbd8f419860`  
		Last Modified: Thu, 11 Jun 2026 00:30:57 GMT  
		Size: 26.2 MB (26245772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6c755c268d7da556d8f9a5e4539c18b88835f20abbcf725eec23af44df29396`  
		Last Modified: Thu, 11 Jun 2026 00:30:56 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a4af8914788dbd3af7ab54ff2a79e0783c4f07cc6b1b0d5573ce0e348a187fb`  
		Last Modified: Thu, 11 Jun 2026 00:30:56 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14f41ac3125a36dae24a8ff555d6b97ff1f683c17a0c70e42e3bea4ec0e4f85e`  
		Last Modified: Thu, 11 Jun 2026 00:30:56 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbb07d90a869645670b8abd56053366aced5ce3f8de48adbf9731e6cca1b35c4`  
		Last Modified: Thu, 11 Jun 2026 00:30:57 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44bec54a37b7a14682554ac910340a49fafcc4c10be206ad85d9b98849b362f9`  
		Last Modified: Thu, 11 Jun 2026 00:30:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:e6c0fc91732f39a19d28e497c3a13bcc5c60ecfc9e295c045202fd308e93ee43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7fa79120c5f9d8971aedae8f4c7f003127bfcca959b8500e71a0fee53cf6cc`

```dockerfile
```

-	Layers:
	-	`sha256:167ee9ac9668af2bf10e72e1a02d28ff0a244aa3b32134c9ec9274d82f190514`  
		Last Modified: Thu, 11 Jun 2026 00:30:56 GMT  
		Size: 2.8 MB (2842368 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8292c90f002e2736b55ad8797d5799f09333b9e3f2fac64246bc30e4c8931b1c`  
		Last Modified: Thu, 11 Jun 2026 00:30:56 GMT  
		Size: 35.3 KB (35305 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:dbb3c16ac62386ff5d1d891e0c67d42514a06525ffa003a145c2b845a2f1c65a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61406825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d607865cd608e923b7f4adbd4a79ecbe2466157e244d6b9ef2262fae7163afef`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:23:48 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 11 Jun 2026 00:23:48 GMT
ENV NGINX_VERSION=1.31.1
# Thu, 11 Jun 2026 00:23:48 GMT
ENV NJS_VERSION=0.9.9
# Thu, 11 Jun 2026 00:23:48 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:23:48 GMT
ENV ACME_VERSION=0.4.1
# Thu, 11 Jun 2026 00:23:48 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:23:48 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:23:48 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:48 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 00:23:48 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:48 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:48 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:48 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:23:48 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:23:48 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:23:48 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:23:48 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22cd640a9e77c2c001e76787eab245c976398aacde898575c94bdc9254e5d27b`  
		Last Modified: Thu, 11 Jun 2026 00:23:58 GMT  
		Size: 31.3 MB (31253685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cebfe1aec587a45029acfb6113c11298c9fbe9785150b2babb442f4cdc1fe10a`  
		Last Modified: Thu, 11 Jun 2026 00:23:57 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bf91cda2eb5bf513aa6aba5cc9ec482bcd9e2f93d18fd521f6d8036b1f9af1f`  
		Last Modified: Thu, 11 Jun 2026 00:23:57 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c089815046bb812d11c4dcf51d9ca73bdb10d92b8aebd9bc6c5165ecf65597ce`  
		Last Modified: Thu, 11 Jun 2026 00:23:57 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50bd6f11c6b9895acfbe79c4ea3f7f44905e88158f1212305db5bf9752136373`  
		Last Modified: Thu, 11 Jun 2026 00:23:59 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08b26d898d4f67f9864ac934eecad4345c28e10e4f79793f4ec1f2007ae1f2c6`  
		Last Modified: Thu, 11 Jun 2026 00:23:59 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:65913bccc19c34a9a1b23bcc4c0ce149f3e9fcc9c1a76a16869a73583df64cc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba1e0004e2b99f4e534927661a6afa46bbb46d4468659900442f62d15040629`

```dockerfile
```

-	Layers:
	-	`sha256:432ddfb968aa9fe8e046e8cc7661c26e128c2c07781aa7c1c18947c7e551d2be`  
		Last Modified: Thu, 11 Jun 2026 00:23:58 GMT  
		Size: 2.8 MB (2817959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e41ce4a384eeec804dba2b72d1034182556fe8bc998831bbb26f4c288dcbd94a`  
		Last Modified: Thu, 11 Jun 2026 00:23:57 GMT  
		Size: 35.4 KB (35353 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; 386

```console
$ docker pull nginx@sha256:46ce83694f5ef6c87a7fda4e282a271d573c136b3bf5a95896e7bdd44f8a56f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63476934 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8157d18307727ff7d9319491c89b27bd845e0bdf5b934c5ad559c739d7c37a27`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:24:57 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 11 Jun 2026 00:24:57 GMT
ENV NGINX_VERSION=1.31.1
# Thu, 11 Jun 2026 00:24:57 GMT
ENV NJS_VERSION=0.9.9
# Thu, 11 Jun 2026 00:24:57 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:24:57 GMT
ENV ACME_VERSION=0.4.1
# Thu, 11 Jun 2026 00:24:57 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:24:57 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:24:57 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:24:57 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 00:24:57 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:24:57 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:24:57 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:24:57 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:24:57 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:24:57 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:24:57 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:24:57 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b31ba7168ac07cbf7c34ab23c8d81bcd70c1727af37431a4663387c9b9674001`  
		Last Modified: Thu, 11 Jun 2026 00:25:07 GMT  
		Size: 32.2 MB (32171137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1db0bc9a2ea43271f5318f1700bb5d3665a206e048a2b5586a7f534c452659e1`  
		Last Modified: Thu, 11 Jun 2026 00:25:05 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c59089c0cde85d00a65531867a1ebf30799f06d9d7aac4ef5fdc96a818de6e1`  
		Last Modified: Thu, 11 Jun 2026 00:25:05 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a991fb1947ac744297036d1d2e25975bd7d876ad6cdd990e34532fe4a1025e7`  
		Last Modified: Thu, 11 Jun 2026 00:25:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d622b341c895ce8fd8a5262cc5792e5f31c8affa16419da5a6efc6e7745cd11`  
		Last Modified: Thu, 11 Jun 2026 00:25:07 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a6cca8356a4a2b760a06cc2cd30b0a02af11669b9b86077b7d8d3be801ea07`  
		Last Modified: Thu, 11 Jun 2026 00:25:07 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:4d0111de8a59361190c070c959e08261053a7ce66884525b1f64d1c2682ba528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abdb8dd2b2c9a1a32dfe9de21fc3a91e74332829d4259868d43cfd03cbec7e24`

```dockerfile
```

-	Layers:
	-	`sha256:15951b1b5eee5a0fb19de63aad1ca1e0743096dfd795aecbf454465793b2b676`  
		Last Modified: Thu, 11 Jun 2026 00:25:06 GMT  
		Size: 2.8 MB (2837319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:386a44752ac1db20ae87c0f9235af6dcd1c7f748e8b99c3d720bf5babbedc3f6`  
		Last Modified: Thu, 11 Jun 2026 00:25:05 GMT  
		Size: 35.1 KB (35115 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; ppc64le

```console
$ docker pull nginx@sha256:a002de24eab8f77926db637780455345c5889eefc8d1cc874db190a17828b5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67222860 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d017af461b15af96e7c48d83b5cbd45b5c1131c4a9d83bdc443d9cecd4ba9a2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Fri, 22 May 2026 18:38:29 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 18:38:29 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 18:38:29 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 18:38:29 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 22 May 2026 18:38:29 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 18:38:29 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 22 May 2026 18:38:29 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 22 May 2026 18:38:29 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:38:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 18:38:30 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:38:30 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:38:30 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:38:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 18:38:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 18:38:31 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 18:38:31 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 18:38:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40094ad8ea10bf9446ede1b9acdf0989062dad70b4ada2e5a56c2977a4dd0b36`  
		Last Modified: Fri, 22 May 2026 18:38:52 GMT  
		Size: 33.6 MB (33617809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0e4c4ddec336e4563f2052a3e88857e8d4b21e69c57781ea19b261921f1bc2d`  
		Last Modified: Fri, 22 May 2026 18:38:50 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d131349f2f15b4dd6f34db769fbc0246d00e35c21828649241c2e3cf170a05eb`  
		Last Modified: Fri, 22 May 2026 18:38:50 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b60c1779e12811806a7a0613a91e40e1a4e5e7f463c001ecd0f8de696f91a34d`  
		Last Modified: Fri, 22 May 2026 18:38:51 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6c70d3fcaf2c1c8d53618ecf9624bec20c7303d7907988878f1774f86b53f02`  
		Last Modified: Fri, 22 May 2026 18:38:51 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63b5caf6558dff2b568526963e23409b0f49cee39adaf869c99e07622885081a`  
		Last Modified: Fri, 22 May 2026 18:38:52 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:ba6f0a6a4443b25b9fc1861bc0e9c4aa3a123588f84194718631bb3ac6e3c9c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab535b7aec72dab88dffc28965558a0f996cb9a979bd550f77a47b1fcf37370d`

```dockerfile
```

-	Layers:
	-	`sha256:933006cc4afda04e3cc083a4ce649320006b2ad6bfca4c5e883abaa00b2ec0fc`  
		Last Modified: Fri, 22 May 2026 18:38:51 GMT  
		Size: 2.8 MB (2844905 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa17e683a289f4dfacfca3e7d8e8ae7033b515bbcd8804aa8097e74d1757ceaa`  
		Last Modified: Fri, 22 May 2026 18:38:51 GMT  
		Size: 35.3 KB (35257 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; riscv64

```console
$ docker pull nginx@sha256:43355baf998910122517322def9e5fc13b8d37d8e5dd6edf8e13c8945a4bbe18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.8 MB (57771514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9df9a99db80b553fcaddd2190e0063c95e3ec863b965f1d6443444e8b65e36ab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Fri, 22 May 2026 23:32:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 22 May 2026 23:32:19 GMT
ENV NGINX_VERSION=1.31.1
# Fri, 22 May 2026 23:32:19 GMT
ENV NJS_VERSION=0.9.9
# Fri, 22 May 2026 23:32:19 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 22 May 2026 23:32:19 GMT
ENV ACME_VERSION=0.4.1
# Fri, 22 May 2026 23:32:19 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 22 May 2026 23:32:19 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 22 May 2026 23:32:19 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 23:32:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 22 May 2026 23:32:20 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 23:32:20 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 23:32:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 23:32:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 22 May 2026 23:32:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 22 May 2026 23:32:20 GMT
EXPOSE map[80/tcp:{}]
# Fri, 22 May 2026 23:32:20 GMT
STOPSIGNAL SIGQUIT
# Fri, 22 May 2026 23:32:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ee2d4de5943bade40807a78dba9a522e201b6f4c325deb12da595911a75f5c2`  
		Last Modified: Fri, 22 May 2026 23:33:51 GMT  
		Size: 29.5 MB (29489321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca04bd93f15ddf251139f93afb5b2af0961e85f8421d3207fdcefcc389958bec`  
		Last Modified: Fri, 22 May 2026 23:33:47 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d848ffd228a41ea2634663bdc8e11009966fb8143143b6fa0d87724e75b9ab11`  
		Last Modified: Fri, 22 May 2026 23:33:46 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51d599c9c3ff2e1cd96b441c8b434f99f5e5731c7f81fc55e2c4924470cbc888`  
		Last Modified: Fri, 22 May 2026 23:33:47 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07aae7ec6126cc559027f2f5dd3d550f0a4c313eff93dee95048dcba403d9847`  
		Last Modified: Fri, 22 May 2026 23:33:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:beac29caa13c9f211a076743939796eb66af7a5080dc96319a141d5f2bee313b`  
		Last Modified: Fri, 22 May 2026 23:33:48 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:d715285180a3e9e148a7845d9946212163277062824a8424cfd4d3cd2c910ac3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:578d43685e203ef4b839c1b13de557eef89fc3ce0936111bed075cdc000c1fa2`

```dockerfile
```

-	Layers:
	-	`sha256:6d6719eb9b073f94866c51c4b722b185ab24d44ebf4bcf1062286b9fed2a8e14`  
		Last Modified: Fri, 22 May 2026 23:33:47 GMT  
		Size: 2.8 MB (2834692 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e12287c7f04834c7bc80e6f5e25a8e518ba9a39bcc5abb82aa9e675bb90f3c75`  
		Last Modified: Fri, 22 May 2026 23:33:46 GMT  
		Size: 35.3 KB (35255 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; s390x

```console
$ docker pull nginx@sha256:396772ee1b7292ca3807966b975400e773b49636ef1efa06b4433785d1423856
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60652021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e754a6ed0937273ccf852243a7946815a763a473d67781676d7677569457243b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 00:29:12 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 11 Jun 2026 00:29:12 GMT
ENV NGINX_VERSION=1.31.1
# Thu, 11 Jun 2026 00:29:12 GMT
ENV NJS_VERSION=0.9.9
# Thu, 11 Jun 2026 00:29:12 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:29:12 GMT
ENV ACME_VERSION=0.4.1
# Thu, 11 Jun 2026 00:29:12 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:29:12 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 11 Jun 2026 00:29:12 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="b151aac903a6fc121d57f0909415381d0a1c1bbd"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="72c13cfedc25a6c1e01c24dd1f736b0fefd1ef7f73ef569e2726fc99c0137327d2e71c8694bd8b0157be2a7247ec1769904746a852e7698caf7df8a5b0040440 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:12 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 11 Jun 2026 00:29:12 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:12 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:12 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:12 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 11 Jun 2026 00:29:12 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 11 Jun 2026 00:29:12 GMT
EXPOSE map[80/tcp:{}]
# Thu, 11 Jun 2026 00:29:12 GMT
STOPSIGNAL SIGQUIT
# Thu, 11 Jun 2026 00:29:12 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec68649151bb28ebc8044a666b1a4cd706d0df0fad0ca082ad7f2263bf38f8b4`  
		Last Modified: Thu, 11 Jun 2026 00:29:30 GMT  
		Size: 30.8 MB (30796059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8c2efab605f4d5e922fc7ff8c3dd7cc88a1cbe0cbc08326b3725ec49178ab57`  
		Last Modified: Thu, 11 Jun 2026 00:29:30 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c426e1d5371353549a595caf0eea48f74d3f0f4d69d2715654169f5d544d16`  
		Last Modified: Thu, 11 Jun 2026 00:29:29 GMT  
		Size: 960.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53fb0f0332af6dd673e0c4506e80c689d889247a22fe2c8b0236164b6cce793`  
		Last Modified: Thu, 11 Jun 2026 00:29:30 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c22a658a7e8277383991d6f6012f7e2704dfa5baf0fcb8afe8e8d6c407441b9`  
		Last Modified: Thu, 11 Jun 2026 00:29:30 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed253e4dde34c9fff5f155888790af2ae789473943bf35751c88f988eb9bff6e`  
		Last Modified: Thu, 11 Jun 2026 00:29:31 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:435b79193ffb91e5955dfec79ec0ab826951cccc0132ac0f0737cbeb994b8b05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201239c39a57aefa60e5e6b956fc25527dc939123774e14a6015f100f8c360f8`

```dockerfile
```

-	Layers:
	-	`sha256:bf19c921a448a0e4fbaad40b3f902af811ebe66a9ac92b3d7a96e6e888132ad2`  
		Last Modified: Thu, 11 Jun 2026 00:29:29 GMT  
		Size: 2.8 MB (2750769 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a1f464fa76ab2e4060a397af827bb48bf289751f626599478b2b8cbd78e5666`  
		Last Modified: Thu, 11 Jun 2026 00:29:30 GMT  
		Size: 35.2 KB (35176 bytes)  
		MIME: application/vnd.in-toto+json
