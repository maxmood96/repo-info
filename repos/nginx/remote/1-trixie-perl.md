## `nginx:1-trixie-perl`

```console
$ docker pull nginx@sha256:3c3d898c978b8fcaa6c2efec807a3fcaf3c37d1cd4f7ac5b02222cd9d87a7b78
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

### `nginx:1-trixie-perl` - linux; amd64

```console
$ docker pull nginx@sha256:a203df3cc32d1bebde9c49fac3b4df0dcedb8b512da87841a18b88097c08b57e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75095441 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55971c0d88d338cd104bdc35393b78920870966c2bb53431910702d72d71b71f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:23:03 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 16 Mar 2026 22:23:03 GMT
ENV NGINX_VERSION=1.29.6
# Mon, 16 Mar 2026 22:23:03 GMT
ENV NJS_VERSION=0.9.6
# Mon, 16 Mar 2026 22:23:03 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:23:03 GMT
ENV ACME_VERSION=0.3.1
# Mon, 16 Mar 2026 22:23:03 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:23:03 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:23:03 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:23:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Mar 2026 22:23:03 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:23:03 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:23:03 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:23:03 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:23:03 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:23:03 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:23:03 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:23:03 GMT
CMD ["nginx" "-g" "daemon off;"]
# Mon, 16 Mar 2026 23:21:15 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:980067d12da26ef4650b40be3a47f7fd80d78d082c3bfa4941f0ad5bde8d2cd9`  
		Last Modified: Mon, 16 Mar 2026 22:23:13 GMT  
		Size: 33.2 MB (33155106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4174e33a2c9eaca1b0da039cf5be29d07469f55e5487747f895331bbd363e4d7`  
		Last Modified: Mon, 16 Mar 2026 22:23:12 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b40784e48373a3bf13d6037f02d6f0a1dfdbd9338e2e4db1474348149445e0d`  
		Last Modified: Mon, 16 Mar 2026 22:23:12 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0b77348d9b01103e73db96486c7f8b81a03b84e0ce526b42909f9c89e95d135`  
		Last Modified: Mon, 16 Mar 2026 22:23:12 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0289d65812c3508dec4114340bc4c2069ab0b6fad93fb216c1d364ac94a1b6b1`  
		Last Modified: Mon, 16 Mar 2026 22:23:13 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9baba07a35b67b80bf4a4b6e428dd098be8f9c5bf462903991f8442d6d2954dc`  
		Last Modified: Mon, 16 Mar 2026 22:23:13 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303f61878d56aa43897bd33d46ad73b4d525928a0eff4db2dc8795790e8e7068`  
		Last Modified: Mon, 16 Mar 2026 23:21:25 GMT  
		Size: 12.2 MB (12160238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:ac0b166c52a9c49f08556413225a1913e67925fae3de66c00492fc4e9fda46ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4265139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a87735f7dff93a124c32c176a7b32473650068f1103c4899e93f37554390ddb5`

```dockerfile
```

-	Layers:
	-	`sha256:5e7a2fd6f2405e234c906bba56103067d3d4113ca14cd3f00c4eba1b462a1a3f`  
		Last Modified: Mon, 16 Mar 2026 23:21:24 GMT  
		Size: 4.2 MB (4240681 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9991c03e916bf1d9240966c016aab220ae77ebb29ed45f004f065efd29ced1c1`  
		Last Modified: Mon, 16 Mar 2026 23:21:24 GMT  
		Size: 24.5 KB (24458 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-perl` - linux; arm variant v5

```console
$ docker pull nginx@sha256:ddad54812d9c34909d52e753b2e80992181aa1db54a6715fab20e006cdc6b831
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66093165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4cf95687204b2baae775702b1aa7de81378edf96a6660f3aef2c1f52fddf6e4`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:28:15 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 16 Mar 2026 22:28:15 GMT
ENV NGINX_VERSION=1.29.6
# Mon, 16 Mar 2026 22:28:15 GMT
ENV NJS_VERSION=0.9.6
# Mon, 16 Mar 2026 22:28:15 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:28:15 GMT
ENV ACME_VERSION=0.3.1
# Mon, 16 Mar 2026 22:28:15 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:28:15 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:28:15 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:28:15 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Mar 2026 22:28:15 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:28:15 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:28:15 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:28:16 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:28:16 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:28:16 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:28:16 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:28:16 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 17 Mar 2026 00:30:39 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e31bb29e314750c7f352a23b779c238e100c03c3ed608350f9697e36bea99047`  
		Last Modified: Mon, 16 Mar 2026 22:28:25 GMT  
		Size: 26.2 MB (26199005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633bb2b56c61d243abd31542aa3034630db7a3e02002db35f931f67247b32d9b`  
		Last Modified: Mon, 16 Mar 2026 22:28:24 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:711c6424c6511647796eaac09313fdc78d5ab843c6de18ae5d05f14cfda83e9b`  
		Last Modified: Mon, 16 Mar 2026 22:28:24 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2e380405cb46928b02c2a7091bea0733fbefb4e45d705934524d0aa08a22b20`  
		Last Modified: Mon, 16 Mar 2026 22:28:25 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbef4395a60d3a87df8834045844dbd50baa1eb2e096dff06cbd11ff04121f9e`  
		Last Modified: Mon, 16 Mar 2026 22:28:25 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c07599bac8dcb43f2ce872c22ee9ea3e06d01852a090a2a734af0fa6e8fb1577`  
		Last Modified: Mon, 16 Mar 2026 22:28:25 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63102c61d8dcbe58b14cea58d62757de8f3179f51ce21807bbfa5f673b0026e1`  
		Last Modified: Tue, 17 Mar 2026 00:30:48 GMT  
		Size: 11.9 MB (11945912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:09c9c3999bd0544f78566287f88f786eeab86f8ae3aa1905b484be6f332b1ed1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4297323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4e4e49edd06b75834833d1b2c0ede01ae7dc4c5bd8a9b09aed9090540862db8`

```dockerfile
```

-	Layers:
	-	`sha256:28621a28f4ae13348d6fa6cbe3872410f4e4ba9b39babb8bcc0cc7fe26b8f1e8`  
		Last Modified: Tue, 17 Mar 2026 00:30:48 GMT  
		Size: 4.3 MB (4272738 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b8ff9c4b2bbc7b535267f18b5a2fa2657049b86f104a2e87850d02bff445fb7`  
		Last Modified: Tue, 17 Mar 2026 00:30:48 GMT  
		Size: 24.6 KB (24585 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-perl` - linux; arm variant v7

```console
$ docker pull nginx@sha256:48ad177b5b4fc2bb7447c1c124ca99eb2b45a08c88c962de1bd9de08a32fd466
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64108844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec81db4dc48a55ef7e00a0ba9836ca9a1ec06f04c0138212c58216ef4c86f5db`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:29:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 16 Mar 2026 22:29:51 GMT
ENV NGINX_VERSION=1.29.6
# Mon, 16 Mar 2026 22:29:51 GMT
ENV NJS_VERSION=0.9.6
# Mon, 16 Mar 2026 22:29:51 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:29:51 GMT
ENV ACME_VERSION=0.3.1
# Mon, 16 Mar 2026 22:29:51 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:29:51 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:29:51 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:29:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Mar 2026 22:29:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:29:51 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:29:51 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:29:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:29:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:29:51 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:29:51 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:29:51 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 17 Mar 2026 00:46:23 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b8b8236bc8f07026dee7d4b01a6bb62e4e4a14e9cfc55c3af99161fe7fbe87`  
		Last Modified: Mon, 16 Mar 2026 22:30:00 GMT  
		Size: 26.1 MB (26138684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e305893650804ce05515f824607b8da001349e14a39a372ca412285f2ec4790f`  
		Last Modified: Mon, 16 Mar 2026 22:30:00 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1164883fee6c30d0d56a82735cb9a295c4650ea8b04f6573be95cec728d998d6`  
		Last Modified: Mon, 16 Mar 2026 22:30:00 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4f32d7c26a5f71dd4f492dde26b5f84ab4d5b581490d8fd0faf1d37ca20000`  
		Last Modified: Mon, 16 Mar 2026 22:30:00 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e137aec23891c09f0c6471763a7a7abc9ca81577e9fbe56433aa7d94df2dbc`  
		Last Modified: Mon, 16 Mar 2026 22:30:01 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a95a1ee77207e1437645801d83442af0968fd6cd30c7643f6423b68fed89358e`  
		Last Modified: Mon, 16 Mar 2026 22:30:01 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bad4f77e314bfa669ec54b1d3e1eaa9c254999a6817d18802d13f89572ce9b3`  
		Last Modified: Tue, 17 Mar 2026 00:46:32 GMT  
		Size: 11.8 MB (11756053 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:bf7fdfae875b87cb81b6a73b4b0af19f0cea1f26df91eefbf86500c09e01885d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4296845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59f6bae95482150de18aea5560a0d9ae35e834a08fd03d1529afab5c2b40b06f`

```dockerfile
```

-	Layers:
	-	`sha256:352558092e1aece120101788ca09185d9ff773131945ddc32ab7576c1d26e69d`  
		Last Modified: Tue, 17 Mar 2026 00:46:32 GMT  
		Size: 4.3 MB (4272259 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2559f3c12bb362446ec92b01b087d02f6d2d5fda336ee97e6af1cd5fede5a57e`  
		Last Modified: Tue, 17 Mar 2026 00:46:32 GMT  
		Size: 24.6 KB (24586 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-perl` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:95435e950cbade8199bb0e9d05f973f233678046fd1ceca544bfe5c12eadc1f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.4 MB (73383507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df54683fb7d217360194be92f1b03d1042ef79cf5346addecec524583b11efae`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:22:45 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 16 Mar 2026 22:22:45 GMT
ENV NGINX_VERSION=1.29.6
# Mon, 16 Mar 2026 22:22:45 GMT
ENV NJS_VERSION=0.9.6
# Mon, 16 Mar 2026 22:22:45 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:22:45 GMT
ENV ACME_VERSION=0.3.1
# Mon, 16 Mar 2026 22:22:45 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:22:45 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:22:45 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:22:45 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:22:45 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:22:45 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:22:45 GMT
CMD ["nginx" "-g" "daemon off;"]
# Mon, 16 Mar 2026 23:26:05 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d322dac342b6fd2003a33b74eebdbb4d48e41e1f0e1f5e74f954f4427c9362`  
		Last Modified: Mon, 16 Mar 2026 22:22:55 GMT  
		Size: 31.1 MB (31135659 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bf7833cbb884e4308b225edf054563c8209bc3c1af22184eb6fc69bd4a09b0c`  
		Last Modified: Mon, 16 Mar 2026 22:22:54 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39db0d317f1e6829b5e10fa2fed607eca1250b2c6f28737e11c92edebb5183eb`  
		Last Modified: Mon, 16 Mar 2026 22:22:54 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcc43639f11c826527333461fc557189a213400ecf77f531bcb82d6bcfeaa15c`  
		Last Modified: Mon, 16 Mar 2026 22:22:55 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6dd09f2dc2e1675cc0ffacf3ec4749412dfb5b23c6c923f91c39385a3071179a`  
		Last Modified: Mon, 16 Mar 2026 22:22:56 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a86953cc5f550cdd05a4c5d4dd5710017045d0b260dc0372248e4c248e16c6`  
		Last Modified: Mon, 16 Mar 2026 22:22:56 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ec6dce5bc622c15ac31f92dd4e990c6ff928878a81be93d471f2cb830c843eb`  
		Last Modified: Mon, 16 Mar 2026 23:26:15 GMT  
		Size: 12.1 MB (12104841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:5773964d13158ef801883bc863b6f557245ac5634f68e17f1bf88a4114e9a7f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4271841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe4fdbec226b6c1f459fcfbe57951f6945928126b747839cf3e82444cddd65b0`

```dockerfile
```

-	Layers:
	-	`sha256:5ae22935e3d6591b2cbbe2b4960b0fa9dc93412eef4854dee90e10de8ef02c41`  
		Last Modified: Mon, 16 Mar 2026 23:26:14 GMT  
		Size: 4.2 MB (4247207 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857087c3253ede430910596904455d0f16080aae78d6e4cdff04a6a07a983e98`  
		Last Modified: Mon, 16 Mar 2026 23:26:14 GMT  
		Size: 24.6 KB (24634 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-perl` - linux; 386

```console
$ docker pull nginx@sha256:f7ad3408a5ac953c384e4614cea3908e1e14d88339dc4596d746bc79d1049392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.5 MB (75503103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5bcbe20fc99cfced63e30b19e3868bb926a736f56fe1731331f38253fa436cd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:25:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 16 Mar 2026 22:25:21 GMT
ENV NGINX_VERSION=1.29.6
# Mon, 16 Mar 2026 22:25:21 GMT
ENV NJS_VERSION=0.9.6
# Mon, 16 Mar 2026 22:25:21 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:25:21 GMT
ENV ACME_VERSION=0.3.1
# Mon, 16 Mar 2026 22:25:21 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:25:21 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 22:25:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:25:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Mar 2026 22:25:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:25:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:25:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:25:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 22:25:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 22:25:21 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 22:25:21 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 22:25:21 GMT
CMD ["nginx" "-g" "daemon off;"]
# Mon, 16 Mar 2026 23:37:02 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82e7c25f9e8abf9ef5cfbc5a0425b67353d47c087355ea39279d77ff65be523b`  
		Last Modified: Mon, 16 Mar 2026 22:25:31 GMT  
		Size: 32.0 MB (32025575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13e14da442a8765191bca55ab92fbd87ea7b0195ec3a782f0482b81e68ed1cf5`  
		Last Modified: Mon, 16 Mar 2026 22:25:30 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f272c2b0e383128a577bfdb7dae43e0284ffac76092759782884533e2f293870`  
		Last Modified: Mon, 16 Mar 2026 22:25:30 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a62f5a9c7fa79bc848c49a88889d698de9be2df067f5c8eaa02832b2eda821d5`  
		Last Modified: Mon, 16 Mar 2026 22:25:30 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daf2a89fdc6695dff0c444b964366d88feec0e398d31429de2647ba80b3415b9`  
		Last Modified: Mon, 16 Mar 2026 22:25:31 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eb7cc6e4d718b5d61940fa260e67fc27e3bc889fda3a9685f387a3acfc434a1`  
		Last Modified: Mon, 16 Mar 2026 22:25:31 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1697b7c3adeb8b7280ddfd8b1b2ad3ae7ce1e3aabd67df4f999a2af1bfa05ed8`  
		Last Modified: Mon, 16 Mar 2026 23:37:11 GMT  
		Size: 12.2 MB (12181798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:1c8e440cb947c6f2c22bbdd183a80ef63308992d9d8cfb3f85b8d91895e3bc04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4292091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594609addd67585a9fb97aa326b3af8eb0a1d9196ddee215912693981f7b29b6`

```dockerfile
```

-	Layers:
	-	`sha256:ed3b7e3d0783ed964b9ba0c7f8d468c864e4861bfeeb87b24274df098c626d69`  
		Last Modified: Mon, 16 Mar 2026 23:37:10 GMT  
		Size: 4.3 MB (4267695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23798abb324b052fa50e13553a64c4150d458878740613a01a616fd179b81645`  
		Last Modified: Mon, 16 Mar 2026 23:37:10 GMT  
		Size: 24.4 KB (24396 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-perl` - linux; ppc64le

```console
$ docker pull nginx@sha256:41aadcf3bb0c48fe629969dc23e062c8c7fd7bd4376cdffe17646cb751f0bc1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.0 MB (79981411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5909048726e7c5b3bfcc1cbfab68ff579a6df7a76a0013604988210c9332ed9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 00:08:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 17 Mar 2026 00:08:05 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 17 Mar 2026 00:08:05 GMT
ENV NJS_VERSION=0.9.6
# Tue, 17 Mar 2026 00:08:05 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 17 Mar 2026 00:08:05 GMT
ENV ACME_VERSION=0.3.1
# Tue, 17 Mar 2026 00:08:05 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 17 Mar 2026 00:08:05 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 17 Mar 2026 00:08:05 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 00:08:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 00:08:06 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 00:08:06 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 00:08:06 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 00:08:06 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 00:08:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 00:08:06 GMT
EXPOSE map[80/tcp:{}]
# Tue, 17 Mar 2026 00:08:06 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 00:08:06 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 17 Mar 2026 05:34:11 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4c21979e4a3c2bced7fd2b5bdc94bfdf005f31a246ecf0f4e526da4684a87f1`  
		Last Modified: Tue, 17 Mar 2026 00:08:27 GMT  
		Size: 33.5 MB (33483832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f70a9c6e24bc941c96b566347451e1dc53125fa76a9d46a711230d251e004f`  
		Last Modified: Tue, 17 Mar 2026 00:08:26 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbfc98798127373e8214ebf070ac8a1652c0a83692884e8876776d3a2132fc34`  
		Last Modified: Tue, 17 Mar 2026 00:08:26 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65f9bd0ca8fc455ef8fbd76479d69cf0d939d2c07c27e547c44d60cf486579c0`  
		Last Modified: Tue, 17 Mar 2026 00:08:26 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc470143449a613d7ef5318b37d08bf7bf3b8542bf4fd284204a026ae581ef42`  
		Last Modified: Tue, 17 Mar 2026 00:08:27 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c7722fa85707853ed55e619a4fad8369535cec2bbfc5a7f51cf2be2e3406c433`  
		Last Modified: Tue, 17 Mar 2026 00:08:27 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a09241ea8d9f229ccbd30100300f2b882688186680cb38c64a607859bfb49dfe`  
		Last Modified: Tue, 17 Mar 2026 05:34:35 GMT  
		Size: 12.9 MB (12900148 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:40610136a33835ce2f24d69cd1dfae87c9457f04f43e94f739a80c5b2fdd8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4303453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35cc795bd9eff9d50bda3fe7fff80f2cc1782cf709b2763ff625d31f672679cd`

```dockerfile
```

-	Layers:
	-	`sha256:88019f61abdb1dcd8b1e21aea1a249b1d877116dd63d31984f1e54ff1a8afc21`  
		Last Modified: Tue, 17 Mar 2026 05:34:34 GMT  
		Size: 4.3 MB (4278915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ea0e94bd2ddc55793be7cee3f7f084763668c40efc012dc074aa09755d4f4d5e`  
		Last Modified: Tue, 17 Mar 2026 05:34:34 GMT  
		Size: 24.5 KB (24538 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-perl` - linux; riscv64

```console
$ docker pull nginx@sha256:6d95a3cec582e1dff7d2e3b5c6ed159e41376bd45dee9397ecd8cbeee4dfa66f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69762921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1179d38e0e5023c5968e9add396ebd2044baa7ca5e4cbd09886b1c9cf63b0960`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 11 Mar 2026 04:23:58 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 11 Mar 2026 04:23:58 GMT
ENV NGINX_VERSION=1.29.6
# Wed, 11 Mar 2026 04:23:58 GMT
ENV NJS_VERSION=0.9.6
# Wed, 11 Mar 2026 04:23:58 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 11 Mar 2026 04:23:58 GMT
ENV ACME_VERSION=0.3.1
# Wed, 11 Mar 2026 04:23:58 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 11 Mar 2026 04:23:58 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 11 Mar 2026 04:23:58 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 11 Mar 2026 04:23:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 11 Mar 2026 04:23:58 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 11 Mar 2026 04:23:58 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 11 Mar 2026 04:23:58 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 11 Mar 2026 04:23:59 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 11 Mar 2026 04:23:59 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 11 Mar 2026 04:23:59 GMT
EXPOSE map[80/tcp:{}]
# Wed, 11 Mar 2026 04:23:59 GMT
STOPSIGNAL SIGQUIT
# Wed, 11 Mar 2026 04:23:59 GMT
CMD ["nginx" "-g" "daemon off;"]
# Wed, 11 Mar 2026 14:06:22 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76b47ccab8b5c499fa3101f76bc86e990326b84f2f34ce9cefb3d1b3fa304dfe`  
		Last Modified: Wed, 11 Mar 2026 04:25:28 GMT  
		Size: 29.4 MB (29369325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc222de52c35d19298e96333f0928eb9f5b14ed43f8076590d581cd4b88c0d5`  
		Last Modified: Wed, 11 Mar 2026 04:25:24 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2dedd8fc86de23d58763ae048297f4ed2ced17a3445c18da6e13ff27a70a7b`  
		Last Modified: Wed, 11 Mar 2026 04:25:24 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1be0cbb56308b196f538898cc50d1038b31441ea189084538ed30b5cf47852a`  
		Last Modified: Wed, 11 Mar 2026 04:25:24 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aad8f7baaf0892bf38605ecea7007a49af6c5af312e1ae46de0b80a3fcc851a4`  
		Last Modified: Wed, 11 Mar 2026 04:25:25 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964dc7c4299e243b2edf47d6314d67bda9b141e4683b039957b33681fc27cc52`  
		Last Modified: Wed, 11 Mar 2026 04:25:25 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54d3b9a23385b08e8f0468f567cfbc09706dc6e6babaa43e48eafd69bae7360a`  
		Last Modified: Wed, 11 Mar 2026 14:08:05 GMT  
		Size: 12.1 MB (12112572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:8344ce1301b79f9b2d2498f6da3ffc0bb23c14305139f371a6800cecfafcff06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.3 MB (4287615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e92ae1e0612644d033d240d92031bbf84c4eae3b4ea1f62f916fcb69025f3b21`

```dockerfile
```

-	Layers:
	-	`sha256:8bd4790789947fe6e130f8d5e894be33e731073d0a11b706005e91b23b680201`  
		Last Modified: Wed, 11 Mar 2026 14:08:03 GMT  
		Size: 4.3 MB (4263077 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d29f6c7b6681a3c01b70c628bcf8f03928a09aed0ecbf8876340c691f64c08b4`  
		Last Modified: Wed, 11 Mar 2026 14:08:02 GMT  
		Size: 24.5 KB (24538 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie-perl` - linux; s390x

```console
$ docker pull nginx@sha256:3a43c165d039e91290f87a2f0eee0cd0116d1b9ef126b86314ba075105c30576
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.7 MB (73678335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd55b8691edfb5f465d62987e358875b4d9f267a44332544eb78b13a4c256e7f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:06:06 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Mon, 16 Mar 2026 23:06:06 GMT
ENV NGINX_VERSION=1.29.6
# Mon, 16 Mar 2026 23:06:06 GMT
ENV NJS_VERSION=0.9.6
# Mon, 16 Mar 2026 23:06:06 GMT
ENV NJS_RELEASE=1~trixie
# Mon, 16 Mar 2026 23:06:06 GMT
ENV ACME_VERSION=0.3.1
# Mon, 16 Mar 2026 23:06:06 GMT
ENV PKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 23:06:06 GMT
ENV DYNPKG_RELEASE=1~trixie
# Mon, 16 Mar 2026 23:06:06 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 23:06:06 GMT
COPY docker-entrypoint.sh / # buildkit
# Mon, 16 Mar 2026 23:06:06 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 23:06:06 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 23:06:06 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 23:06:06 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Mon, 16 Mar 2026 23:06:06 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Mon, 16 Mar 2026 23:06:06 GMT
EXPOSE map[80/tcp:{}]
# Mon, 16 Mar 2026 23:06:06 GMT
STOPSIGNAL SIGQUIT
# Mon, 16 Mar 2026 23:06:06 GMT
CMD ["nginx" "-g" "daemon off;"]
# Tue, 17 Mar 2026 01:22:55 GMT
RUN set -x;     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-perl=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in module-perl; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make module-perl             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi # buildkit
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06d3492f60a12b35ddbe000d85a6bbe2192adb52e860ac88a75a331b02c2645`  
		Last Modified: Mon, 16 Mar 2026 23:06:22 GMT  
		Size: 30.7 MB (30652052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:574fa7e577cf02faa3dd59fc0880137cf168b774472eb6f646153fc077b54e96`  
		Last Modified: Mon, 16 Mar 2026 23:06:21 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:157f92bd79981eedf6b43f4a86d9a30aa9fa8d3631de07b5ac89c2646fb7132c`  
		Last Modified: Mon, 16 Mar 2026 23:06:21 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:563e5465c8a43263c1fdaafb5a75dedd87f81b30017b64cc52a717d344affa76`  
		Last Modified: Mon, 16 Mar 2026 23:06:21 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22479fdaca7531ffe986ee018fb4463bff56539a1a092d852d4a7ab60833fff7`  
		Last Modified: Mon, 16 Mar 2026 23:06:22 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26ea755e57b2f5ec1909183f8f700d0723f11218ab6bc4dc83674d8dc6ee6fc6`  
		Last Modified: Mon, 16 Mar 2026 23:06:22 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:540a9d6f71f32b63079c3e16b8edebc6c51451e93bf6ab7e7767502442f50de5`  
		Last Modified: Tue, 17 Mar 2026 01:23:11 GMT  
		Size: 13.2 MB (13186414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie-perl` - unknown; unknown

```console
$ docker pull nginx@sha256:563766abbc8544d733c7d15630d01b8b6216b494120e2bfe69d527e4f24f3f2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **4.2 MB (4205978 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc9651598fee60878deca657b197450c34a526c37ddac6f3323c435034480200`

```dockerfile
```

-	Layers:
	-	`sha256:56232b6035220ed407b558fb57c02721a75d2955641fb684971f4db066c40f85`  
		Last Modified: Tue, 17 Mar 2026 01:23:10 GMT  
		Size: 4.2 MB (4181521 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e72a78f666f4510a6d7700f057849828fbf69851905db9e9782dcb9582df360b`  
		Last Modified: Tue, 17 Mar 2026 01:23:10 GMT  
		Size: 24.5 KB (24457 bytes)  
		MIME: application/vnd.in-toto+json
