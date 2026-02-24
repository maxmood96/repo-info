## `nginx:mainline-trixie`

```console
$ docker pull nginx@sha256:44d1be91d34f545895e9b422036782123c63e4cd4a11bbfc20bfe53ac59f7798
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
$ docker pull nginx@sha256:b7f90eb243ff5e2c4a7dc61768160e888ac459e2c05aeb1b3bdf90920aa9d7e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62923184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd204fe2f75024354b1f979d38cc43def9e049cc2df1cda45074d1b84c4f9b3e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:05:02 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Feb 2026 19:05:02 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 24 Feb 2026 19:05:02 GMT
ENV NJS_VERSION=0.9.5
# Tue, 24 Feb 2026 19:05:02 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:05:02 GMT
ENV ACME_VERSION=0.3.1
# Tue, 24 Feb 2026 19:05:02 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:05:02 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:05:02 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:05:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 19:05:02 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:05:02 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:05:02 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:05:02 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:05:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:05:02 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:05:02 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:05:02 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b47f187216b68c3f90b7fb9a947a76d4bd2981a8f469cb6092e7da5d9efea014`  
		Last Modified: Tue, 24 Feb 2026 19:05:12 GMT  
		Size: 33.1 MB (33139958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ad233904a1166fd3832d9657b163937f66c906795a517a87b516bc3f2481695`  
		Last Modified: Tue, 24 Feb 2026 19:05:11 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eedda9fd87862df4b2eccd3da9f2e38122124dec2e4217b530bd48d809b3840b`  
		Last Modified: Tue, 24 Feb 2026 19:05:11 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ff83c394d65bf2c49f844ba18fe2e8121fe07e1f3f92325c05246319b98f7e`  
		Last Modified: Tue, 24 Feb 2026 19:05:12 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17d0911eaf62f5c4c34e54943d30dbb0d86b8ad614c80ef5ee0249ff54a3373e`  
		Last Modified: Tue, 24 Feb 2026 19:05:12 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df0b66c867e491634d63f065ef5ea556cba20a97761039f9e9d5af71442f8fbf`  
		Last Modified: Tue, 24 Feb 2026 19:05:12 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:c9ae80bdecfccb6d4bfa29b55458364c71ae4058e91ba46206f9f9b0210debb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f9722971b8be179bc640a0aeeb739b53832dfc17f14e97c0c39b0cca86e70f0a`

```dockerfile
```

-	Layers:
	-	`sha256:c13150b54a537c9676aa0e45c42f907a858b95bd1934675f67c9a7c5ab669b84`  
		Last Modified: Tue, 24 Feb 2026 19:05:12 GMT  
		Size: 2.8 MB (2817223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0019bbecc57254263f286f9377e0950c98c558a2fd7d933b375a71d2315cc196`  
		Last Modified: Tue, 24 Feb 2026 19:05:11 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:baed2e48cc37440b5a3f598b4a5ceb9ee0a8f65e368065135cd44c55f4428f3e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54116367 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b59ba66ffdab2068ff09e69d2ec6350f75092d316590156cc4be8178fdab3a10`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:08:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Feb 2026 19:08:19 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 24 Feb 2026 19:08:19 GMT
ENV NJS_VERSION=0.9.5
# Tue, 24 Feb 2026 19:08:19 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:08:19 GMT
ENV ACME_VERSION=0.3.1
# Tue, 24 Feb 2026 19:08:19 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:08:19 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:08:19 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 19:08:19 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:19 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:19 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:19 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:19 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:08:19 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:08:19 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:08:19 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:280a075cc1d2a97445b9f4430aa9774bfc38fc4217b7fc9d6a7b04e7e431cb65`  
		Last Modified: Tue, 24 Feb 2026 18:42:44 GMT  
		Size: 27.9 MB (27947608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49737a431cc7eb1a94bdbec855ca8bf3ba6981eb5da80ecdc6ab1c0dde2a3c47`  
		Last Modified: Tue, 24 Feb 2026 19:08:28 GMT  
		Size: 26.2 MB (26164153 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb070e6e7be2a2866cdda793ef18509c0e06501d020f194f1bc3ff9809057306`  
		Last Modified: Tue, 24 Feb 2026 19:06:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a077c9b0c9bc493ae1b26f3de404cb6cef55774ceebc98d1d4dcaca38aa5d803`  
		Last Modified: Tue, 24 Feb 2026 19:08:27 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd71475040ee05c0b0b0049e0ea3ba42d9e4ba003efc34be0c12d9f080feeda`  
		Last Modified: Tue, 24 Feb 2026 19:08:27 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb16f59e64b8e80ad052891bac23fe336feb8b15d06113cea516c167c384aa0a`  
		Last Modified: Tue, 24 Feb 2026 19:08:28 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4db84a78dd6744337ba311afd7706315609ff233c667bd9d707242e02458d896`  
		Last Modified: Tue, 24 Feb 2026 19:08:28 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:2ce43b9dbcd10ba645aeb486f695ee7112af51a8ca4664fe74c5b89a760281b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2878647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31b4d74c6cf29d99e93ca0103d831eed88c29834db6322d90ae45d14edeb2753`

```dockerfile
```

-	Layers:
	-	`sha256:a68ca1c6bc075625474b299f51ee028e9fcde7e80b6d9642a3e4753c88b66f1b`  
		Last Modified: Tue, 24 Feb 2026 19:08:27 GMT  
		Size: 2.8 MB (2843363 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f27c8905347abb684181749778acf2d0d8b3c15d14053d22106cbc4f5e84d9a`  
		Last Modified: Tue, 24 Feb 2026 19:08:27 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:6f1cef39cc1d02db681ebca268a6f63c4e830413ea7abbd3697ad1d490f0ca33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52324358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d64056ed1f459c9e6ad96c7fdcfe09e1ba5762adef668ca2c06aa8f77d7c212`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:12:36 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Feb 2026 19:12:36 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 24 Feb 2026 19:12:36 GMT
ENV NJS_VERSION=0.9.5
# Tue, 24 Feb 2026 19:12:36 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:12:36 GMT
ENV ACME_VERSION=0.3.1
# Tue, 24 Feb 2026 19:12:36 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:12:36 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:12:36 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:12:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 19:12:36 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:12:36 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:12:36 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:12:36 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:12:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:12:36 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:12:36 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:12:36 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:be1f02cfc6708a9e39fcae481bc45544f342901641dd63341104a8ef3fa3cde9`  
		Last Modified: Tue, 24 Feb 2026 18:42:48 GMT  
		Size: 26.2 MB (26213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4004126aa51ad0f89653f59cb8dcda5bbeef700bee18796d9a692419554242a`  
		Last Modified: Tue, 24 Feb 2026 19:12:45 GMT  
		Size: 26.1 MB (26106009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3109a85a257bd320d1b45d48c569d3a5373cf88dd2d3cb261a4485d066a647`  
		Last Modified: Tue, 24 Feb 2026 19:12:44 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e8cced27a2ed62c9bc1c6a4714224442144b683b3234ffe380264968efa2288`  
		Last Modified: Tue, 24 Feb 2026 19:12:44 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:163c61b9ff348cff04031c4115c09e86835b146a79eaab5bb0191923363493de`  
		Last Modified: Tue, 24 Feb 2026 19:12:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3687a16cd78f9dcbe623e2f9420c4bcb6820e8cc60deeae761a1fcc61a9d8ed`  
		Last Modified: Tue, 24 Feb 2026 19:12:45 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:155c865e4b22da8b96aa17562b8ce5426c3eeebc6bab858acc3bd064f04c4975`  
		Last Modified: Tue, 24 Feb 2026 19:12:45 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:a68a88813bd83aa63978f214a4eefd774d3973bbab09af450f936253f5187aac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5e948ffba514c295db5f6bd820568bce5e0ea163d39cb3c2afcaae88f71b2e8`

```dockerfile
```

-	Layers:
	-	`sha256:133fc388ccb3abc13bc4744d84eef53f63155056e42e0cbde24eed60f60c3d40`  
		Last Modified: Tue, 24 Feb 2026 19:12:44 GMT  
		Size: 2.8 MB (2842108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:96470f96e3aba83f8c4b5a5e8b9424ba41f2d8275461a109b914092cf6f2ea46`  
		Last Modified: Tue, 24 Feb 2026 19:12:43 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:3040aee8d792887190feb77276924597cf8a50cb9304723816a5e68047d49b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61246389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af158aaca82baec54d1538e2d858778fa0c0a0a5787535657df463ef1a8cc05`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1769990400'
# Wed, 04 Feb 2026 23:52:44 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 04 Feb 2026 23:52:44 GMT
ENV NGINX_VERSION=1.29.5
# Wed, 04 Feb 2026 23:52:44 GMT
ENV NJS_VERSION=0.9.5
# Wed, 04 Feb 2026 23:52:44 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 04 Feb 2026 23:52:44 GMT
ENV ACME_VERSION=0.3.1
# Wed, 04 Feb 2026 23:52:44 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 04 Feb 2026 23:52:44 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 04 Feb 2026 23:52:44 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 04 Feb 2026 23:52:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 04 Feb 2026 23:52:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 04 Feb 2026 23:52:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 04 Feb 2026 23:52:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 04 Feb 2026 23:52:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 04 Feb 2026 23:52:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 04 Feb 2026 23:52:45 GMT
EXPOSE map[80/tcp:{}]
# Wed, 04 Feb 2026 23:52:45 GMT
STOPSIGNAL SIGQUIT
# Wed, 04 Feb 2026 23:52:45 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3ea009573b472d108af9af31ec35a06fe3649084f6611cf11f7d594b85cf7a7c`  
		Last Modified: Tue, 03 Feb 2026 01:15:22 GMT  
		Size: 30.1 MB (30140064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efc7865cf13e460368cc89c201ba74f7b1e16fd489c647dd9e7c986fefb0da44`  
		Last Modified: Wed, 04 Feb 2026 23:52:55 GMT  
		Size: 31.1 MB (31101736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5380ffdd215e97bce8fae5707d8307604544cb5a9db084290e144412e65c63e0`  
		Last Modified: Wed, 04 Feb 2026 23:52:54 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb8853dab2dabaa33ac144ddfea9f5601edc994cf38763fb8d3b9f7207b89d0c`  
		Last Modified: Wed, 04 Feb 2026 23:52:54 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1063666c8b8e795e6f8b7da6d7698e4cb8b50b7c49690c297131d16a36789bfa`  
		Last Modified: Wed, 04 Feb 2026 23:52:54 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e9ba714bdf166e853fd20a64cb9578030aee1cc891a5db8cf08c0e584c71a57`  
		Last Modified: Wed, 04 Feb 2026 23:52:55 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58072fb4fd7c2ee1925f1e45856b849481d10e4fdd51699cfa96849e010d58c0`  
		Last Modified: Wed, 04 Feb 2026 23:52:55 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:0f336a9e059822eec6a7a95e02918bb81ee9d2f401895d29a4edd52af09ebdcc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:049cb188b35f3e3c3a86ee71cc2d2f1ce9f29b86b66e78067700ab7b5f3630e2`

```dockerfile
```

-	Layers:
	-	`sha256:875ddf4f8f5c5cf05a1cd1773bd8fa4c52576bf48d7f0b066cc29c69e8fdc113`  
		Last Modified: Wed, 04 Feb 2026 23:52:54 GMT  
		Size: 2.8 MB (2817707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee66459a851ff558a15620b8deb90759d229bc1616e4b2d71f06aca196c65d9e`  
		Last Modified: Wed, 04 Feb 2026 23:52:54 GMT  
		Size: 35.3 KB (35332 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; 386

```console
$ docker pull nginx@sha256:86df83a58a60cc7097f08b9b4b37bd35663eefc28dbb15ef4a17ed58cb3c1ea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63297134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d65845c3da39da867c5fb93fc0483313e4db6f81a74e0fcb17a8b6a34bdd186`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1769990400'
# Thu, 05 Feb 2026 00:00:00 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 05 Feb 2026 00:00:00 GMT
ENV NGINX_VERSION=1.29.5
# Thu, 05 Feb 2026 00:00:00 GMT
ENV NJS_VERSION=0.9.5
# Thu, 05 Feb 2026 00:00:00 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 05 Feb 2026 00:00:00 GMT
ENV ACME_VERSION=0.3.1
# Thu, 05 Feb 2026 00:00:00 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 05 Feb 2026 00:00:00 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 05 Feb 2026 00:00:00 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 05 Feb 2026 00:00:00 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 05 Feb 2026 00:00:00 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 05 Feb 2026 00:00:00 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 05 Feb 2026 00:00:00 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 05 Feb 2026 00:00:00 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 05 Feb 2026 00:00:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 05 Feb 2026 00:00:00 GMT
EXPOSE map[80/tcp:{}]
# Thu, 05 Feb 2026 00:00:00 GMT
STOPSIGNAL SIGQUIT
# Thu, 05 Feb 2026 00:00:00 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:169fd34ed51dc04ba419a375bd69752b6d59f872027dfb0b9fc2763b36ffde10`  
		Last Modified: Tue, 03 Feb 2026 01:15:01 GMT  
		Size: 31.3 MB (31293855 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d08097c10c6c76036c4c23326bae4ce4807a4c06c113d14f0926f3c642289240`  
		Last Modified: Thu, 05 Feb 2026 00:00:13 GMT  
		Size: 32.0 MB (31998691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e47634195385bb0d4e7061f4592fae6b76b5d18dd98a0d2566616daf49fa7dc`  
		Last Modified: Thu, 05 Feb 2026 00:00:11 GMT  
		Size: 625.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63aaffabab42ba03c42df7461c484ad01c3d6a8e0576071550164566ac01efba`  
		Last Modified: Thu, 05 Feb 2026 00:00:11 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e940ccf0d40d76e785eb1dbafc0d2595234c733d9faf57bb39838338159432`  
		Last Modified: Thu, 05 Feb 2026 00:00:11 GMT  
		Size: 402.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65916754f5f920afd7a4d2f62ff1e351447d6e93ec60f6b969007a1f88022a3b`  
		Last Modified: Thu, 05 Feb 2026 00:00:13 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47a05324babff51fdc489309cd54e2a8ba6b3114cbda4632f734e6432e74ef86`  
		Last Modified: Thu, 05 Feb 2026 00:00:13 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:5e32fe26df26b3c90e8b351b9f35ff2b204090398b9f4bd7ac07579fe2856cfa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1805e008072bb0675834c1c476ff0fab054dcd3e7f2d941c57caf47a0c0d151`

```dockerfile
```

-	Layers:
	-	`sha256:e0099be13e7cb9e0a8f38c8df83cc40b5c9ec8c506be3ead4f0ef951a3d3e469`  
		Last Modified: Thu, 05 Feb 2026 00:00:11 GMT  
		Size: 2.8 MB (2837059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d117192f9dd24de176b3b8be386443a8d3b0f1e5d162d7ed76e40a79bad468e1`  
		Last Modified: Thu, 05 Feb 2026 00:00:13 GMT  
		Size: 35.1 KB (35094 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:f012505466ba5e5b217976fdb40168074c5e4e51beda444dff292e74345f06f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67039293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb69cde8ca7cbfb09e784f756f4baa61819dc0e64c7f2fd941e396fef6e38478`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:32:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Feb 2026 19:32:05 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 24 Feb 2026 19:32:05 GMT
ENV NJS_VERSION=0.9.5
# Tue, 24 Feb 2026 19:32:05 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:32:05 GMT
ENV ACME_VERSION=0.3.1
# Tue, 24 Feb 2026 19:32:05 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:32:05 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:32:05 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:32:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 19:32:06 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:32:06 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:32:07 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:32:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:32:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:32:08 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:32:08 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:32:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:91416f8238d93c33a42d4030b8a24944e7f5b4b808e36e206f1bf078f8543c0d`  
		Last Modified: Tue, 24 Feb 2026 18:45:10 GMT  
		Size: 33.6 MB (33600216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88b4c207755d36a926d2bf0ff17253915cbafdcf1a100a114301501610d19053`  
		Last Modified: Tue, 24 Feb 2026 19:32:29 GMT  
		Size: 33.4 MB (33434472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e564395aa0ca365d2be1b944f668ff67308653ee8d72fe5a7715c325527349a6`  
		Last Modified: Tue, 24 Feb 2026 19:32:28 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f64ecb253cca07694bc8acf6d5d80786a5ff3102a891fa8e688ec47db34c2a9`  
		Last Modified: Tue, 24 Feb 2026 19:32:28 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5d11d3ddcc46f370d3636ca6551461fbcf008df5b3a90f00d1aefbd2171477b`  
		Last Modified: Tue, 24 Feb 2026 19:32:28 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482180b665d25eaf075dad20c74f6831dbc32bcf3ce3b175869cbff7bb84428d`  
		Last Modified: Tue, 24 Feb 2026 19:32:29 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7adef432f4c4963b6790181ca786b86740b898ed7db86a045b624a171c38572`  
		Last Modified: Tue, 24 Feb 2026 19:32:29 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:31a204f324ac375efc479b4db38fe9b8ab6d0ddb57d5e3099e46fd553ddc69b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2879989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a30397eee68150f0b40533282c6748809c8dd1bc63ca3493856daa11908f61`

```dockerfile
```

-	Layers:
	-	`sha256:e5987d1f5343eb702b85077c4856fad8df7377dabb034a8a350873a9ba191572`  
		Last Modified: Tue, 24 Feb 2026 19:32:28 GMT  
		Size: 2.8 MB (2844753 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73f4b0e501bee5b67e092956953a375b1e7c76829c591513f52b3e5c00618bf6`  
		Last Modified: Tue, 24 Feb 2026 19:32:28 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:523414bd9d4a340382411ce598b54b949295e07bb19ef16542cbfde06e93386a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57608252 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a0834b19206d2ad68a08434e94f00968c5ba800f7453cf3d8ef67aeb7f7d2f0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1769990400'
# Fri, 06 Feb 2026 00:54:59 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 06 Feb 2026 00:54:59 GMT
ENV NGINX_VERSION=1.29.5
# Fri, 06 Feb 2026 00:54:59 GMT
ENV NJS_VERSION=0.9.5
# Fri, 06 Feb 2026 00:54:59 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 06 Feb 2026 00:54:59 GMT
ENV ACME_VERSION=0.3.1
# Fri, 06 Feb 2026 00:54:59 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 06 Feb 2026 00:54:59 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 06 Feb 2026 00:54:59 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 00:54:59 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 06 Feb 2026 00:54:59 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 00:54:59 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 00:55:00 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 00:55:00 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 06 Feb 2026 00:55:00 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 06 Feb 2026 00:55:00 GMT
EXPOSE map[80/tcp:{}]
# Fri, 06 Feb 2026 00:55:00 GMT
STOPSIGNAL SIGQUIT
# Fri, 06 Feb 2026 00:55:00 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:4526db52defd9278f79daec64ebfa633041460dbe0cfad19564ae34d84b13b4c`  
		Last Modified: Tue, 03 Feb 2026 07:14:46 GMT  
		Size: 28.3 MB (28276389 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22d788dcb1b70c4a2cef00ebe5e1e38b06ca9593ee9d088a0bd218641719bce0`  
		Last Modified: Fri, 06 Feb 2026 00:56:32 GMT  
		Size: 29.3 MB (29327260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e822088e5b8f488a3fcb6f01ccba743390355a3fdca095a910ed305dd9a8dc1`  
		Last Modified: Fri, 06 Feb 2026 00:56:27 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d260562d8a2e2f326021711e7c3a6b3b2dcb2f9f28b6fda604517682293f3b6`  
		Last Modified: Fri, 06 Feb 2026 00:56:27 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c735bba1b74c9d5b8742bfc3721d7e303fe768200301f7a2e8f234c93ba8c0b`  
		Last Modified: Fri, 06 Feb 2026 00:56:27 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d835d8a10a1470d18303d4c4726a87ac07a9de075bac3a905bde2201c5ada0`  
		Last Modified: Fri, 06 Feb 2026 00:56:28 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4faea9394830542cc7b42e94d920f307eac454f46fee00eeca53136843e3f592`  
		Last Modified: Fri, 06 Feb 2026 00:56:29 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:904629b49fc2e2a68086386dda08765e53c622fc921b8231865014b12edf16fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57269225b7eb955439acbb82e9bd5a2434743500b9f6535b029cc337954ccbc3`

```dockerfile
```

-	Layers:
	-	`sha256:cebf6acb15855c81fec95978fe28a567f5b8520cb8632456c4fe9706cdd7fa00`  
		Last Modified: Fri, 06 Feb 2026 00:56:28 GMT  
		Size: 2.8 MB (2834540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b8a85fb7dea67755ed7cbc9feeb6cd75d860cb334aadd5fb6f424c60f374eda5`  
		Last Modified: Fri, 06 Feb 2026 00:56:27 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:78c1dcc9ab8725145e34aea900814cabe7f98a7b8ef5404dda50a93e3ac476fd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60465736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c9ef01d98f9ed32e7e4df220b51b102d5f0ec6ee0d6bae40724c139470ecc42`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:14:25 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Feb 2026 19:14:25 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 24 Feb 2026 19:14:25 GMT
ENV NJS_VERSION=0.9.5
# Tue, 24 Feb 2026 19:14:25 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:14:25 GMT
ENV ACME_VERSION=0.3.1
# Tue, 24 Feb 2026 19:14:25 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:14:25 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:14:25 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:14:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 19:14:27 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:14:28 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:14:30 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:14:31 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:14:31 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:14:31 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:14:31 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:14:31 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b50f587e37cdad2c774c5137974987f2b5aca2ef491f293c135b60e1e43e0135`  
		Last Modified: Tue, 24 Feb 2026 18:43:50 GMT  
		Size: 29.8 MB (29838179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f8374ced3dbf82ac3b71970c7be30d99048dcd44d2becaf9073fecf0d565621`  
		Last Modified: Tue, 24 Feb 2026 19:14:59 GMT  
		Size: 30.6 MB (30622954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a69d709745ad12165ab17bcf73a41be5763eb79f236d2bebb8e8ecd9e2cb03c`  
		Last Modified: Tue, 24 Feb 2026 19:14:55 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61cc798151e31fd33bdf4d21d53687522a53c0ae454eddd297a9813456dae5ec`  
		Last Modified: Tue, 24 Feb 2026 19:14:55 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:123a14398199e4d71053b94eecba40ef0c26fc09c70fa3a34fe327faa5332761`  
		Last Modified: Tue, 24 Feb 2026 19:14:55 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:214fe574f804cf582e154eb933e2eb0388cb560b2c45f47a35fb5ba6121da1b8`  
		Last Modified: Tue, 24 Feb 2026 19:14:56 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dea44848752ffe98cf2eeabad97709e022f063d27a012c9b7abc4fefc43a9140`  
		Last Modified: Tue, 24 Feb 2026 19:14:56 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:fce376b4223f859208bd8e6b2aab32a80a05da055de2112bfde6a19c6da6f402
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64dedeaf32eb35240c0c4a076d8e97093c625c0dd5c6254493c36dae87da95ce`

```dockerfile
```

-	Layers:
	-	`sha256:06b5d43bcdf8568d2bdb3255e9d62e125d27012602667b8e402998f7a827abd1`  
		Last Modified: Tue, 24 Feb 2026 19:14:55 GMT  
		Size: 2.8 MB (2750509 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00b610b74784c2d0ed139cd6ded9a5157a527e4c697e20a79dbf84f663c902ef`  
		Last Modified: Tue, 24 Feb 2026 19:14:55 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json
