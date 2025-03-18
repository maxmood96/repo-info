## `nginx:mainline`

```console
$ docker pull nginx@sha256:ffa524536736e9341b829e0638f56afab8bda691b8cfa46c1f02ffe4c6046f97
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

### `nginx:mainline` - linux; amd64

```console
$ docker pull nginx@sha256:54809b2f36d0ff38e8e5362b0239779e4b75c2f19ad70ef047ed050f01506bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72159831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a18edff8091d5faff1e42b4d885bc5f0f897873b0b8f0ace236cd5930819b0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eaa34f5b9c2a13ef2217ceb966953dfd5c3a21a990767da307be1f57e5a1e4f`  
		Last Modified: Mon, 17 Mar 2025 23:13:07 GMT  
		Size: 44.0 MB (43950370 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:417c4bccf5349be7cd4ba91b1a2077ecf0ab50b3831bb071ba31f2c8bac02ed1`  
		Last Modified: Mon, 17 Mar 2025 23:13:05 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7e0ca015e553ccff5686ec2153c895313675686d3f6940144ce935c07554d85`  
		Last Modified: Mon, 17 Mar 2025 23:13:05 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:373fe654e9845b69587105e1b82833209521db456bdc5bc26ac7260e3eb2dd52`  
		Last Modified: Mon, 17 Mar 2025 23:13:05 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97f5c0f51d43d499970597eef919f9170954289eff0c5d7b8f8afd73dbb57977`  
		Last Modified: Mon, 17 Mar 2025 23:13:06 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c22eb46e871ad1cda19691450312c6b5c25eb5e6836773821d8091cffb6327cc`  
		Last Modified: Mon, 17 Mar 2025 23:13:06 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:286178150929ca8f03b8bae94a053295262258d4556df3a1c109e262c71e8e4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2990691 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f40ddffdd19f88457ca7f7e9995bdfdd0965081dde6f492b168c10eccb84b90`

```dockerfile
```

-	Layers:
	-	`sha256:6ec57245ce5311e50ffe016ffe4a6b85b4c873cf067c345692f4ea981936605c`  
		Last Modified: Mon, 17 Mar 2025 23:13:05 GMT  
		Size: 3.0 MB (2956072 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2754baa73ec501f43dc30fb0ce84d2749604be1c2152dcd54c818f4a03c78c1c`  
		Last Modified: Mon, 17 Mar 2025 23:13:05 GMT  
		Size: 34.6 KB (34619 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v5

```console
$ docker pull nginx@sha256:7b78424d471d32f3b7f016de5b6f9da65fbf41bbca56eaa65e98e75bf02aa3eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62444796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08ba260178dd0bdf60b44659735f9a587e2a1bb17546ee0c1f12351657a3040e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1742169600'
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
	-	`sha256:87c352465466fcf04c9686fee29c2541af5fc39172801545bb24d9faa8cdeabb`  
		Last Modified: Mon, 17 Mar 2025 22:17:36 GMT  
		Size: 25.7 MB (25735853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee35602e2c9c56f68727f865413f056f068f01656aca1fef8f28aca398f7d67f`  
		Last Modified: Tue, 18 Mar 2025 03:33:53 GMT  
		Size: 36.7 MB (36704343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:125f57df8963011eeecbfae6cf7f045757c4c789e769ba81a41db3b837fd596d`  
		Last Modified: Tue, 18 Mar 2025 03:33:52 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42b7dbcce9185e782717b9a417238679efe26a522b52318ac153d2045739c8d5`  
		Last Modified: Tue, 18 Mar 2025 03:33:52 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fcd4d263b08bfc21fba5539a3850784408fdbcfb55f9167a04df25af5061ebfc`  
		Last Modified: Tue, 18 Mar 2025 03:33:52 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08fe222d4ca0a6dfab36ff136e12978f2433d87335607ed53756a11f3959d432`  
		Last Modified: Tue, 18 Mar 2025 03:33:53 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb2c9632d0f8c644c840a65fac7262f278c8e1d783e828b3a42c80a7610bf57`  
		Last Modified: Tue, 18 Mar 2025 03:33:53 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:ec5fe78b07775c4e5def2d671279ddde48eabc8b37ec3544bcd6b19a7e8dfbf6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3012038 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63d1babdaec75752b7a40790aab4cb66ce0e5ed5faa2ff42a5d5ad6ab0d26f0a`

```dockerfile
```

-	Layers:
	-	`sha256:4b9828489e2eaacad63b7f34af8c4a8374f9d444b2c7cc53fc31483759977c91`  
		Last Modified: Tue, 18 Mar 2025 03:33:52 GMT  
		Size: 3.0 MB (2977295 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a11c2a786926a2348138e9fed863756c2875468379fae6ebd04f7c0c8ad39323`  
		Last Modified: Tue, 18 Mar 2025 03:33:52 GMT  
		Size: 34.7 KB (34743 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v7

```console
$ docker pull nginx@sha256:4a3424cc81d2ccddb86f7223e7632c07e053db8556d079c9fb66df54dcf601e3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60727437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d631ceac303c5ce8314b65215be8e50992ef25017666114d7b11397c8f589bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1740355200'
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
	-	`sha256:b47565bb13c54d9e609fa36aeddfc2e70b47de981bac54a6d090c2148f2f4fc4`  
		Last Modified: Tue, 25 Feb 2025 01:30:40 GMT  
		Size: 23.9 MB (23919734 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e2c8703a8d59bd1f785f850208d9a378f5421f4e9f381edbe9a17e5e7a7e83`  
		Last Modified: Tue, 25 Feb 2025 02:36:05 GMT  
		Size: 36.8 MB (36803102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85c7f314cf25682537ba9698b889aad8877d9af415a3bcb4480d48a33e8a7419`  
		Last Modified: Tue, 25 Feb 2025 02:36:03 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7244ad71181b69c64d8127fca4bc6f2cf170485d607f72048d17561466a7d96`  
		Last Modified: Tue, 25 Feb 2025 02:36:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd4c781a9d754a5b9ae86a94a4e4d44b290f6780e00910df8cb68407010e0006`  
		Last Modified: Tue, 25 Feb 2025 02:36:04 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a30ed3e263606a28c7320134c3e5220432b19d41cfbfb36d0f252e84ac9555fc`  
		Last Modified: Tue, 25 Feb 2025 02:36:04 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3870d0e2aa9ccee3f7cd852e011928fb75f069276a7a3486047e6bb5ecec2f52`  
		Last Modified: Tue, 25 Feb 2025 02:36:04 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:5507edf751ea3f10a54c540be410145283d6ba2a63ab795a8007233da9927a1b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3010993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daca3f9f0b361e929b1dda16605791ec1f2e1818069943926921aa337ad4902`

```dockerfile
```

-	Layers:
	-	`sha256:00a92ed3c5bff90898bbffec22b20d6e15a4e52df6d0f019a386b154fdd7bb1a`  
		Last Modified: Tue, 25 Feb 2025 02:36:04 GMT  
		Size: 3.0 MB (2976250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b7b56a5d1ed2914faa591cb5226b57669193e8b24b4bfc015bf5d810f2a0049c`  
		Last Modified: Tue, 25 Feb 2025 02:36:04 GMT  
		Size: 34.7 KB (34743 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:02571cc661a41d4f341ca335fe6a0471c4be4ca177c0dbe5e8bb350f7c42118b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68617492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678546cdd20cd5baaea6f534dbb7482fc9f2f8d24c1f3c53c0e747b699b849da`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:492c7b58b293d01e3f23c246ea2b3874224b85fe45398bb5905438bb8d283e29`  
		Last Modified: Tue, 25 Feb 2025 02:59:19 GMT  
		Size: 40.6 MB (40564467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:587f328750b8fc449cddf9e8bd2d03207f1a75ac6557928e3fbabb992faf9bdf`  
		Last Modified: Tue, 25 Feb 2025 02:59:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60b452932acd2a22cf1aa6441925e9f68de801ec68b36a9b062355d9f01bafde`  
		Last Modified: Tue, 25 Feb 2025 02:59:18 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60ea76daae04c6cc66775b4034a80d05fa39024a0f95bf7ca33848947968d22`  
		Last Modified: Tue, 25 Feb 2025 02:59:18 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb23ee5f039b978692eec6d76bc46813a4dac001c3ccca2cc239d3349988952c`  
		Last Modified: Tue, 25 Feb 2025 02:59:19 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b59f5cbcfb9c134463863d80d55953176967c498593241cf41e0189fa28d9b9`  
		Last Modified: Tue, 25 Feb 2025 02:59:19 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:6ef2f602db91782fea73cee62e9173ddfd4ea8e57b4f574da85b160a0630c050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (2991306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0bef66c83ecc14fba2d7737e383b90ed1a44249b754be20be471cd3954fcab8`

```dockerfile
```

-	Layers:
	-	`sha256:f26bb434e4b0eebe8e481dcbf96d532b0d396d06fdc04710fbd967e06a2e0f0d`  
		Last Modified: Tue, 25 Feb 2025 02:59:19 GMT  
		Size: 3.0 MB (2956511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:49d4343ab9c4eae3c5f734eec608ab94bddaf381312e7e2be47877c283b289e6`  
		Last Modified: Tue, 25 Feb 2025 02:59:18 GMT  
		Size: 34.8 KB (34795 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; 386

```console
$ docker pull nginx@sha256:6ed673914841c7cdc4dbdc67d0f2c20e0b82884d5034b818aba362e2be1a4335
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70527877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f41d4699cd78e4f3233cc3ea19f668e221f0d489b260300bbf1b6ce6ec844a14`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac1782ed4a408289c6e54660d3fcfb6309d86f6c3220611f3717648d71828113`  
		Last Modified: Mon, 17 Mar 2025 23:30:06 GMT  
		Size: 41.3 MB (41333743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38da88f9121dee79b0d6c876e10943195a65cbca4790c2ea5ada11b462e3f5e3`  
		Last Modified: Mon, 17 Mar 2025 23:30:04 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d86178111244bd5e3b4ec921226115308525ab8cae3a2b8eb258a7b31e480324`  
		Last Modified: Mon, 17 Mar 2025 23:30:04 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:320e6d10c7eeef478c6d01c60c1ec3f12e3fd5747077b716f1281ac706c5d243`  
		Last Modified: Mon, 17 Mar 2025 23:30:04 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd1f8f76dfe2009893d7a3374cbd76cd2e3ac72f5c9a6f1a7d90505ba7007b15`  
		Last Modified: Mon, 17 Mar 2025 23:30:05 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef03d09290b2a856011796c16fe7891eb114b1df7a3d20c4f988810eb1478fd7`  
		Last Modified: Mon, 17 Mar 2025 23:30:05 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:ff4c3eed12b73cea11594d3631f05ee3711e36b0f0a8159234844583137ae9b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3003900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43af9a86297bcb1df44ba78301b50ca8736b437bfb8fc7d1fc1c61696ee38449`

```dockerfile
```

-	Layers:
	-	`sha256:aa27d4dff9fc72e6cdfb997b463cff11f92bc3b11f701387c002aaff3595130e`  
		Last Modified: Mon, 17 Mar 2025 23:30:04 GMT  
		Size: 3.0 MB (2969343 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9fc5c549b926b654c4b9c196d7957c6acac5274c885d7e7576929e4ece30119`  
		Last Modified: Mon, 17 Mar 2025 23:30:04 GMT  
		Size: 34.6 KB (34557 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; mips64le

```console
$ docker pull nginx@sha256:a7784e313763d9624ec5bf5a558c4770e23cf81741ce846dbec31e733514548e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68251380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02911356e72ae14506d0fe9563104796563eadaf5739b0a460546c8485526af8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:1851efe37d59b19d5c7092778464657e31dbfae35874c19fb94fb95542e2fba7`  
		Last Modified: Tue, 25 Feb 2025 01:30:49 GMT  
		Size: 28.5 MB (28493681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e6ce666d2f9da3504b35d99a2c4378190b9570bdd7cf039361234240907d67`  
		Last Modified: Tue, 25 Feb 2025 03:39:25 GMT  
		Size: 39.8 MB (39753098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb400e3813fb1631c16899d9d8d04cebbb7a5870d59a016e54925bee1900fcbc`  
		Last Modified: Tue, 25 Feb 2025 03:39:21 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10537f51fc639ab2212000d093b98b2c526709d228d4d5b087bd9a4e5bc338bb`  
		Last Modified: Tue, 25 Feb 2025 03:39:21 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccb59180a82b20916a82c57fb8ca6ed5d8a3216364945d60cc9de5376ccf193d`  
		Last Modified: Tue, 25 Feb 2025 03:39:21 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:904b4112073ba3d62e6d4169e1008449b11f20a6e45aa77e48f72413f9d22ca2`  
		Last Modified: Tue, 25 Feb 2025 03:39:22 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0408ba68a244f60d31629b78c859efcd70fde4f1635719aa502df07966b0cb6`  
		Last Modified: Tue, 25 Feb 2025 03:39:22 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:aca4038419a3420ee797ecf80708f909693ee886ba7365bde664d9ee9b2f5b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **34.5 KB (34523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:52681dd64c390cc352807462a7d9cbe10c31abb452f72661c7dcad9d8250c6db`

```dockerfile
```

-	Layers:
	-	`sha256:346e638df3eec4f97b9d41bf27002a7229dd487e705fddd12c5aebfc3c7646e2`  
		Last Modified: Tue, 25 Feb 2025 03:39:21 GMT  
		Size: 34.5 KB (34523 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; ppc64le

```console
$ docker pull nginx@sha256:411f6640c4aa93710e30508e01eec11e1713f48962fafa0d68356ee444c22949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76874077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f61a9fc4337803a80d9b726bae5d32436cb220d94ab210d77c8f0cbd8812986c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1740355200'
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
	-	`sha256:4713de4e13d024eec0b1cb2d083909104c2a36ed3ffba92c5cf710577a33ad45`  
		Last Modified: Tue, 25 Feb 2025 01:30:47 GMT  
		Size: 32.1 MB (32052314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05406d3b9cef30f9efa5883d78f3e718c4266aedd0612af1de057535b0820119`  
		Last Modified: Tue, 25 Feb 2025 02:46:49 GMT  
		Size: 44.8 MB (44817160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a53486a839200f6c792fcbb7af6f717d8bdc34f0e75f6f3be6951f9189c0c34`  
		Last Modified: Tue, 25 Feb 2025 02:46:47 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d35dad5c6b7fc0f090a78c43be53192a5d45f5a07e36612e64b7975efc5c0a92`  
		Last Modified: Tue, 25 Feb 2025 02:46:47 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b16cb9bf49bb9a887632b7969bab598a2905eb92262411d1dd2c8c57a1c5133`  
		Last Modified: Tue, 25 Feb 2025 02:46:47 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:958b77b44a6aab7bcdbbb411f02d11865a840fe4ae629d3718d3c45567db5f45`  
		Last Modified: Tue, 25 Feb 2025 02:46:48 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:057d2730e9456e4013bd92b76344104cbd242b22e84126c7cb6970cfb1a7cd1b`  
		Last Modified: Tue, 25 Feb 2025 02:46:48 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:228a0cff93514df19b8fac54da01fcbb9632a40e90529b0d17c503bf3d6afea9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3018539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1fbc74a42c66bd7392c4c51c0f47f30c294288cc0bc25d5711ad8752d5f71de`

```dockerfile
```

-	Layers:
	-	`sha256:c3697154996fef69b1793737c2f6a93c64fd2646e6953578272b4b01d30fbf8e`  
		Last Modified: Tue, 25 Feb 2025 02:46:47 GMT  
		Size: 3.0 MB (2983841 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:746eac595fd0a1b5f7f7c8af8b8235889611314760c42086a9684d76683fbcd8`  
		Last Modified: Tue, 25 Feb 2025 02:46:47 GMT  
		Size: 34.7 KB (34698 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; s390x

```console
$ docker pull nginx@sha256:7037479647df8e0cd6c365f921c1ac6a1345a3af22f1fbc3c932fc4c4557bcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66861753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4a5f8d7683a698db75d63d69fbf1362f1f06ab614b601b38b498932649df85d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Wed, 05 Feb 2025 21:27:16 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1742169600'
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
	-	`sha256:c25b115468ab81aaa9017d4d794bc086cba904c84f73abda1eac28615cd44629`  
		Last Modified: Mon, 17 Mar 2025 22:27:10 GMT  
		Size: 26.9 MB (26861059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42e76350622c1d08a56358e9d654392f5db2b0fa5ea8e5301ada6a7c6ddce73d`  
		Last Modified: Tue, 18 Mar 2025 04:24:59 GMT  
		Size: 40.0 MB (39996096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d70427f5f7fdd8d4ccff61f12b29e005ab83e6a590aba4242ca8c06f35f10323`  
		Last Modified: Tue, 18 Mar 2025 04:24:58 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de8c590ba8e32eadd2f4485ad18e2ae95e5345501a4a1b6ba92b1215a98cd0e`  
		Last Modified: Tue, 18 Mar 2025 04:24:58 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41fe88c3306fc0f16aec82b76232dd0e4d18e4cf64d4d7845eb2c98f2839ea99`  
		Last Modified: Tue, 18 Mar 2025 04:24:58 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5611f7df2a1143665d32baeb93f499481dc7ceb71d866e69a8dda27212ffd00c`  
		Last Modified: Tue, 18 Mar 2025 04:24:59 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6273026ca9923b23de1f0351450206b1f5907ab7a9d3d3ccfb7807c0d38530af`  
		Last Modified: Tue, 18 Mar 2025 04:24:59 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:c6684d0a865332dae5b08a05fa35e84b9d091196e97f8fd68b2d7b910804c3ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 MB (3002082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e848bd136e4e6cfb876318a71983d2741ce74680687854ab7abee48f03f8daf`

```dockerfile
```

-	Layers:
	-	`sha256:d001c937a7079715f7ae407585372eb01d786b635ed3fab431fd70eaf2415cef`  
		Last Modified: Tue, 18 Mar 2025 04:24:58 GMT  
		Size: 3.0 MB (2967465 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d6495a2bfc82025a2c19e4418a92c8884fc90574e53f191de7ab0798d97a130`  
		Last Modified: Tue, 18 Mar 2025 04:24:58 GMT  
		Size: 34.6 KB (34617 bytes)  
		MIME: application/vnd.in-toto+json
