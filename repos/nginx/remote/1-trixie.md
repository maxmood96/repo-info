## `nginx:1-trixie`

```console
$ docker pull nginx@sha256:dec7a90bd0973b076832dc56933fe876bc014929e14b4ec49923951405370112
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

### `nginx:1-trixie` - linux; amd64

```console
$ docker pull nginx@sha256:dead9cf6bae3a0447c3148dd1afb374a3c8339b8875298bd3130387f64abf879
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62935203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a1e6313642049664ed59099f3ca37a672486049af68395c62dd885a9bf4de35`
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

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:717872295c96e0ffc6081bbb5f325a390cf1a580eb4b0487be1bbb00cd760866
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95cdead27193a95dd596669919eaf66f90b205517f6609e5428958d8d9f8a8e0`

```dockerfile
```

-	Layers:
	-	`sha256:c96ca1f4ddf7fbb0983ad6b46fd9aed63ea1385869bc8ce9c3ee6e9b292e8a8c`  
		Last Modified: Mon, 16 Mar 2026 22:23:12 GMT  
		Size: 2.8 MB (2817261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00238b7dc6b276e8b40c777bd0b32bbfeb43606cead0bf2a84e5c83b19d7a6da`  
		Last Modified: Mon, 16 Mar 2026 22:23:12 GMT  
		Size: 35.2 KB (35155 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:65ffd00d336fb3a6e1b232aefb37c0cfaa3e4ce65b3e45349c284f43667a8403
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54147253 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:60536a1f390b8b297e1d79629048abb4df06c42ca51567faa667412487042b7c`
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

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:7ca67c6e81f6e62d24413981133ebc8ae1ab9e38dfca7af68c0a10239e10eae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2878684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:496addc3e50ae3369549fb0d0c7eb8f6c3b85a737f71e8324122c5e7fb7ddc74`

```dockerfile
```

-	Layers:
	-	`sha256:75542afc85e982a88874f1db9a99e6b3405d8ec6cd96cda4671950e6a1327cdf`  
		Last Modified: Mon, 16 Mar 2026 22:28:24 GMT  
		Size: 2.8 MB (2843401 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:83fee0d5307353577ba25164b69e8e2670bf3b4443ae3de29d5772c54fb3c671`  
		Last Modified: Mon, 16 Mar 2026 22:28:24 GMT  
		Size: 35.3 KB (35283 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:8cac3bc916419c5a352024ac3a0022fda941321ad6a6edcbda067358485904b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52352791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:146775cb7f096ac989e0488565d8a5a8060db1b4835ceb78120860055cd68299`
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

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:b0dd8f6d33fb9db586f1bc8ba43134e490571d39742f0b3487248ea5f12fba7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c49bf3c868da383c3d7ce833832f700f0cd7529613385bc3bc837625fc96315a`

```dockerfile
```

-	Layers:
	-	`sha256:287e74de45fb6cdb9ff53574295cdb235223ffb04792ee7c1f471f474a9fa7c5`  
		Last Modified: Mon, 16 Mar 2026 22:30:00 GMT  
		Size: 2.8 MB (2842146 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6986e6207e7f75be02ebc068e28119d973110710e3907f8865f88c31cb63fed5`  
		Last Modified: Mon, 16 Mar 2026 22:30:00 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:be275332f8853c71c4b5dc5478840381bd43179acae1e9b1c6b93b332e12d14d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61278666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c755eb98e755f546d294f6036b10ec449685c12c2eedef746db9fcaad5bf7638`
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

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:0b53d7624980a876a4a329029ad2c9aeae17e834f6d142260d7c7b90df69f542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e83bf522eebfe7ebbe38ea72e7e70b1817297fcc6932556cc27626a84163496`

```dockerfile
```

-	Layers:
	-	`sha256:37d38c79113382133cc3c004cb41eb1c7615ec6aa05420f8783603e537ee8c75`  
		Last Modified: Mon, 16 Mar 2026 22:22:55 GMT  
		Size: 2.8 MB (2817745 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3920ff1ae89a9450d2643a91601a4031f5d2dda73ccaac913504afdcf8c76feb`  
		Last Modified: Mon, 16 Mar 2026 22:22:55 GMT  
		Size: 35.3 KB (35332 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; 386

```console
$ docker pull nginx@sha256:21c2e155cbb915a5ee36b17d262a73969034134d2782a5150accf2996ff07528
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63321305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3d15cdcc748f6c3a330f2b092762858052abf193164e24d5d0c714cd4973ab`
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

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:1ca6fce0000fd990a321eaf5b8756311255e44364dddba1a4a89a0f10e1771f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:667a22efea6c816ac7a1637e8cca11fc248d950e4cf07402c2920ba6a8f4d16d`

```dockerfile
```

-	Layers:
	-	`sha256:b4d29f84f638a173585c061cdc1764de0716f5f58e97678648b275a8fdbde4c8`  
		Last Modified: Mon, 16 Mar 2026 22:25:30 GMT  
		Size: 2.8 MB (2837097 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f3e87be613974bcf2c3a8e5b26406bd3e30c803225df3d5cba40c103794d7502`  
		Last Modified: Mon, 16 Mar 2026 22:25:30 GMT  
		Size: 35.1 KB (35094 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:bef48fd1306c3bddef2a394e43592ac557843bb6981d304a001983e6a8fa1265
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67081263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5a50580b101e35ac8413caa6f1e9ece339a04e0cabc29dbb6a44ecf9b7a84f`
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

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:fc34fd72cec69c41687834ad683fd19b7ac42686c720ca8eb85cedaf9cb06034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2711d3f6b4ef93b65905445eeb21ee36611f8f9adac588e9ed0e0967c268ed64`

```dockerfile
```

-	Layers:
	-	`sha256:6167b3f75ec1ee6ebed932c76295cd2d84776593551222fc6220bc6fa95a7ae9`  
		Last Modified: Tue, 17 Mar 2026 00:08:26 GMT  
		Size: 2.8 MB (2844791 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b68a06fa78e30fd378402c414b77059c72768b62bedf5f396c955f891128ac9f`  
		Last Modified: Tue, 17 Mar 2026 00:08:26 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:502ea0409ffad87f68355a3265b6178033c5f1d43282e8e6786730b9eb18a242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57647620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20603e007c8ecfcbb0182338c53f74b3fa96c5638dc1fdc85d6cb0db799b0036`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 04:12:19 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 17 Mar 2026 04:12:19 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 17 Mar 2026 04:12:19 GMT
ENV NJS_VERSION=0.9.6
# Tue, 17 Mar 2026 04:12:19 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 17 Mar 2026 04:12:19 GMT
ENV ACME_VERSION=0.3.1
# Tue, 17 Mar 2026 04:12:19 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 17 Mar 2026 04:12:19 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 17 Mar 2026 04:12:19 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 04:12:19 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 17 Mar 2026 04:12:19 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 04:12:19 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 04:12:20 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 04:12:20 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 17 Mar 2026 04:12:20 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 17 Mar 2026 04:12:20 GMT
EXPOSE map[80/tcp:{}]
# Tue, 17 Mar 2026 04:12:20 GMT
STOPSIGNAL SIGQUIT
# Tue, 17 Mar 2026 04:12:20 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43e58d893e7063bf4b4b00e4894f5442ce416140234c13818ee366569269c2fb`  
		Last Modified: Tue, 17 Mar 2026 04:13:51 GMT  
		Size: 29.4 MB (29367378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5e79c29f77dba3c4a7bd068feec528c5031862f7de54630cb2755f7b10b771a`  
		Last Modified: Tue, 17 Mar 2026 04:13:46 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba713864489d5ef3b99aef53d7add99db2cdb50486c52f06be748c9206b9d9a0`  
		Last Modified: Tue, 17 Mar 2026 04:13:46 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b9f306f1671843d7a0c4c9353c51515f4b71f33b970750c5a9f9546e20044cc`  
		Last Modified: Tue, 17 Mar 2026 04:13:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0fa640645fc2d7c9cb77941c6d695572e4c3d27578583f63721544a800bed2`  
		Last Modified: Tue, 17 Mar 2026 04:13:48 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a9a8f09e37dba10092462534521c6f652d0b3e08c84383b5811cbb790838473`  
		Last Modified: Tue, 17 Mar 2026 04:13:48 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:c7616efb727a8c6f5ad3562a04d24328d2f41021fdf81068970cce42f35a46e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869814 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dddfb24b7a62b27902b264e0ac2eb586f0c71d3e3c47fd37c24424af9632dbb`

```dockerfile
```

-	Layers:
	-	`sha256:c16af5622454a7d98f437df77ff2aa978ff93834d2e807decb7b2b17c84834fd`  
		Last Modified: Tue, 17 Mar 2026 04:13:47 GMT  
		Size: 2.8 MB (2834578 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3ccf1197a406cee8e7fca4dcc08fdf0e4877224e303ce6003c23916fec099424`  
		Last Modified: Tue, 17 Mar 2026 04:13:46 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:1-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:23c78d14e4b876e821f9d4ebfa0c5200e23cdf71ff3c3b87018b546cc64199d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60491921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ff01673e2304c444cd3b9f0cbd77f50b499690e40f4ea310be25e36bd4d0e7e`
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

### `nginx:1-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:f6e3c1b05711b4d71903d5e863bef639e8862342fae1bf3d9bdc75bbd8dd0ed6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b66ee756fa6659ce9493f0f67fa9a1824531c88450a6d6607f3eb1be5ce66236`

```dockerfile
```

-	Layers:
	-	`sha256:ddaf2deb25a912a4a24ee97c390a3ec4705f631d0de8bc4465436c5c05a71485`  
		Last Modified: Mon, 16 Mar 2026 23:06:21 GMT  
		Size: 2.8 MB (2750547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af11246e75f0490ffecdf430a01e409c27daebb65a038e29575f2e8dd913c4b3`  
		Last Modified: Mon, 16 Mar 2026 23:06:21 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json
