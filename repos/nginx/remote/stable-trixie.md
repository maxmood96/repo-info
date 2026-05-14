## `nginx:stable-trixie`

```console
$ docker pull nginx@sha256:842a3f99afd73859b5c647f8be6f0000849be286674e30d9dbcf7a6902a69487
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
$ docker pull nginx@sha256:8a54ef9a7571ccf30c383e135583fd572b4ed34115a846c46bb4279152a1a0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63042532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62217789446a0bb2b68d9f65538a7f4246b7041505f42383e5e29f0112644eb3`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Wed, 13 May 2026 19:06:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:06:08 GMT
ENV NGINX_VERSION=1.30.1
# Wed, 13 May 2026 19:06:08 GMT
ENV NJS_VERSION=0.9.8
# Wed, 13 May 2026 19:06:08 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 13 May 2026 19:06:08 GMT
ENV ACME_VERSION=0.4.1
# Wed, 13 May 2026 19:06:08 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:06:08 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:06:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:06:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:06:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:06:08 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:06:08 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:06:08 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:06:08 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:06:08 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:06:08 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:06:08 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8240314804b5dceb7b88dc702ebce78fbb0ecce2e0c2c2b5e694ac20b8087582`  
		Last Modified: Wed, 13 May 2026 19:06:18 GMT  
		Size: 33.3 MB (33257715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec8920bf35081557aa40cf83d440e0f157f6233e72d8d4c32986069385fed66d`  
		Last Modified: Wed, 13 May 2026 19:06:17 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50813b7d3c2dff730374e9c37cbf56e0e3ab6ecb4cc5beeff54a344b97e6be75`  
		Last Modified: Wed, 13 May 2026 19:06:17 GMT  
		Size: 953.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e10fd5b43d5d4d0edfb84513bdc30a44220ccaa165e535afdef7a99ec823eb9`  
		Last Modified: Wed, 13 May 2026 19:06:17 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b1086f6d3cfdf42c1e0805c3cf00d3072e51e4112723a5b8c7539a787b877d`  
		Last Modified: Wed, 13 May 2026 19:06:18 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8970cf8766d45ebfd037a9f6692ae00cef8167b2dce27b8842c610c2caf0a259`  
		Last Modified: Wed, 13 May 2026 19:06:18 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:f5afec71fcd84fe60fac7cc9a4e6e0a3cc215b30c0f0ffa433d7ad8b9dafac5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2850054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:547846dd0f75dc131c7a56b0bd14ccb9257c2f56e800693da5e3c0a6831d8586`

```dockerfile
```

-	Layers:
	-	`sha256:e776c6f2c8b948339b27e22c92250241848bddb2fcb819b1352d2902add31a35`  
		Last Modified: Wed, 13 May 2026 19:06:17 GMT  
		Size: 2.8 MB (2816111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8332c35bf217b8c2161c49b83a45c33c81c3f1a64b07075acfedfeab49e76202`  
		Last Modified: Wed, 13 May 2026 19:06:17 GMT  
		Size: 33.9 KB (33943 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:86f30c544f0d8c2e9999dc88bde044612c591581e18de3181bb490685f7347a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54216844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db65cf91a4099f5f09b75cc3c3abbc1f6ef932b76808f46379faea5d6cb4729`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Wed, 13 May 2026 19:13:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:13:51 GMT
ENV NGINX_VERSION=1.30.1
# Wed, 13 May 2026 19:13:51 GMT
ENV NJS_VERSION=0.9.8
# Wed, 13 May 2026 19:13:51 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 13 May 2026 19:13:51 GMT
ENV ACME_VERSION=0.4.1
# Wed, 13 May 2026 19:13:51 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:13:51 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:13:51 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:13:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:51 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:51 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:13:51 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:13:51 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:13:51 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecf7a1674be52fae5d21df3015d19d6cd92493cd86e9216775a48696db394e76`  
		Last Modified: Wed, 13 May 2026 19:14:01 GMT  
		Size: 26.3 MB (26264048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0ddd4643661841d5c12bc3d46a46feda9d41f881bbbb971f000cbc56f779c70`  
		Last Modified: Wed, 13 May 2026 19:14:00 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9731b2d4bb71773e5417e88d99457ce7e894fd64880f0ebabb032eabcabf993d`  
		Last Modified: Wed, 13 May 2026 19:14:00 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13805938e2494e645e7e20c8bd591a3d2ecb9ad0ccc07895130c53160f24139a`  
		Last Modified: Wed, 13 May 2026 19:14:00 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc1864ddfc6762d6b2ec4df9ea2345f92c239834ea17e9434208123433fe895e`  
		Last Modified: Wed, 13 May 2026 19:14:01 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b99876d78744e7900ae684efde7ca8140e90b6cb297a6b7aad76b3f506a042e`  
		Last Modified: Wed, 13 May 2026 19:14:02 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:143bb068f3315ebbf5c5551fcfbd5891b0fd5dc4a5999b948d56642121fd7bad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f98f41a7e91bfea550bc9712ee6ca93bf5a18d0e7eca14f8ad8bf95478da62ce`

```dockerfile
```

-	Layers:
	-	`sha256:976720b0c145f181b59ef5421b81ade9fd878172e2b6b7d048961c419bc9549c`  
		Last Modified: Wed, 13 May 2026 19:14:01 GMT  
		Size: 2.8 MB (2842219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eddce827f49906d28ebd8180cce349f65c87791acf12055fdb09be234786fb58`  
		Last Modified: Wed, 13 May 2026 19:14:00 GMT  
		Size: 34.0 KB (34039 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b2cf8389033e3f2dff75fe8d5e578a95768943a1fc8927a7923580ae280a9de7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52428422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f142302564a0eee01824570d047b41d2267323cd44ea626cacf8bcd71069f875`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Wed, 13 May 2026 19:15:14 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:15:14 GMT
ENV NGINX_VERSION=1.30.1
# Wed, 13 May 2026 19:15:14 GMT
ENV NJS_VERSION=0.9.8
# Wed, 13 May 2026 19:15:14 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 13 May 2026 19:15:14 GMT
ENV ACME_VERSION=0.4.1
# Wed, 13 May 2026 19:15:14 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:15:14 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:15:14 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:15:14 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:15:14 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:15:14 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:15:14 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:15:14 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:15:14 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:15:14 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:15:14 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:15:14 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dccc5a0581a8385352141b319799507331e638aa0d38ed9f5b17f8e2ddafc36`  
		Last Modified: Wed, 13 May 2026 19:15:24 GMT  
		Size: 26.2 MB (26208908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b43a159a7ffc423cb2622da83539e485d9d5d021aadcffbd9ba7ecdd3d28260e`  
		Last Modified: Wed, 13 May 2026 19:15:23 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb76ff15780d2631cf09cf662a039448dbc7aa134289b45041459464e3dbb2a5`  
		Last Modified: Wed, 13 May 2026 19:15:23 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ba703a56a49fcc95c383383f1f514887c5ee7357d306907a04f075e2be263f0`  
		Last Modified: Wed, 13 May 2026 19:15:23 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f93fb0e455864295230b3489b66e97604a77f1049185f39e35302e2ac803041`  
		Last Modified: Wed, 13 May 2026 19:15:24 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:634dc4543ee75ff476a5012bc58e8535e565cfefb0e27041415d8458c6446f6c`  
		Last Modified: Wed, 13 May 2026 19:15:24 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:e264ea9a4a1d0db43a28313a6012b503df80fb5df56cf92e5587fc4f81c419c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33a998cdf6d97758c0cac7536b96b030991327cd7d04f1a2c5c81224f663d1b`

```dockerfile
```

-	Layers:
	-	`sha256:3c918cffbb31572c892201f5de973975547458f2cf30d6fde1ac5d6f2f47d7ac`  
		Last Modified: Wed, 13 May 2026 19:15:23 GMT  
		Size: 2.8 MB (2840964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5a07c1acc9dbf2ffa4839b02bd1483c3810c17a51fc96ef9533793e180af5f5b`  
		Last Modified: Wed, 13 May 2026 19:15:23 GMT  
		Size: 34.0 KB (34038 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:69aeae7f0ed2c51e44426a4dba5fe411c265eab68afe33331a718910422a1a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.4 MB (61356074 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed999a037c1659715a3c3c95f03aa28bbc3e1a2e91e0d0c4d83af4ed431dbab9`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Wed, 13 May 2026 19:05:35 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:05:35 GMT
ENV NGINX_VERSION=1.30.1
# Wed, 13 May 2026 19:05:35 GMT
ENV NJS_VERSION=0.9.8
# Wed, 13 May 2026 19:05:35 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 13 May 2026 19:05:35 GMT
ENV ACME_VERSION=0.4.1
# Wed, 13 May 2026 19:05:35 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:05:35 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:05:35 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:35 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:05:35 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:05:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:05:35 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:05:35 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:05:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa27a0d3d6150a4f9e7d3bdebe1464fc9f59c59f4f9b90697b91f6b29f3d27a1`  
		Last Modified: Wed, 13 May 2026 19:05:45 GMT  
		Size: 31.2 MB (31207841 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d499092138d80602050ce3d0981b0c48107dbd85d9adece77bb9c6af94c7b344`  
		Last Modified: Wed, 13 May 2026 19:05:44 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecdb41d07e739fc410ab8a75d7f3c09e7bd0ef3b845ab2fc50a2e34bcebd04d`  
		Last Modified: Wed, 13 May 2026 19:05:44 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:714876adf26b0d41591bbc690509c4166fe4b005a7c0cfaa958311b9e1536303`  
		Last Modified: Wed, 13 May 2026 19:05:44 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1b6e93cf5debd26af2169446d48a8b8bf920f669794cb59d369ea9dfcd226b3`  
		Last Modified: Wed, 13 May 2026 19:05:45 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90b651716ae81dc52c08e515cba2183adf22c3192f16b587a1cc5286e656055a`  
		Last Modified: Wed, 13 May 2026 19:05:45 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:33c12cdad8f4687b236dbb0ff4f877d3598aee62df4201788d14adda208a3ed5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2850618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38d4ff41e5d76d8d02b58e94e39dfc01ca828e6acfdafa9e60493a7ef5db801c`

```dockerfile
```

-	Layers:
	-	`sha256:af9753b07340ce10a80ca6cb99e9950ae063adcb7304ef5324f78a2cd161bb91`  
		Last Modified: Wed, 13 May 2026 19:05:44 GMT  
		Size: 2.8 MB (2816547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ddfd05ec26a3908fd82fa6f6e655d6a496d4e8a555023d57e241083506dc1e18`  
		Last Modified: Wed, 13 May 2026 19:05:44 GMT  
		Size: 34.1 KB (34071 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; 386

```console
$ docker pull nginx@sha256:5214bfdd104fb84f58554d420e0f6eb4a9229de981575730409a1db617ccf489
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63423121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15702ad59d47a5e27fdf53fc4bf2ba06ddadec77416311a85729f4f78166e7d2`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Wed, 13 May 2026 19:13:23 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:13:23 GMT
ENV NGINX_VERSION=1.30.1
# Wed, 13 May 2026 19:13:23 GMT
ENV NJS_VERSION=0.9.8
# Wed, 13 May 2026 19:13:23 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 13 May 2026 19:13:23 GMT
ENV ACME_VERSION=0.4.1
# Wed, 13 May 2026 19:13:23 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:13:23 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:13:23 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:23 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:13:23 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:13:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:13:24 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:13:24 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:13:24 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db26e664c6c43f68f198cb3464eff1ca45de79d794927c9498007606f7b3ceea`  
		Last Modified: Wed, 13 May 2026 19:13:35 GMT  
		Size: 32.1 MB (32122118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd4b5c73db40ea8493a307640efd0ffdfb0477bf2ce876893c071953931c627f`  
		Last Modified: Wed, 13 May 2026 19:13:34 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2d6a8d51e664ea312bcc7d20d13d0c4b1d43878202429aec93edbedf90d1e19`  
		Last Modified: Wed, 13 May 2026 19:13:34 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131a85f6ff1dd2c13f7e52ef2ae68428610ca67f750d51d85412e6007d65c63d`  
		Last Modified: Wed, 13 May 2026 19:13:34 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae9185dac504052c01bc404397700005f9081ffefc8dadea4d1d70c4862c460`  
		Last Modified: Wed, 13 May 2026 19:13:35 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3c81577f807f1d3fcce2a8cc0f82317fdc4fd9770b255c43a7fb96b040ae19`  
		Last Modified: Wed, 13 May 2026 19:13:35 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:26b1ad4c605c989a9fca2370ce677789ae31854330cc7d38589f1daded4dea8d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ecb9fc3e849bb9af3b284b17f07455b41f10c035143bbfe833027de7e92e682`

```dockerfile
```

-	Layers:
	-	`sha256:145cf3257325459822863b76497bed1f01845b47e5f8727008694cfa4d6c94f6`  
		Last Modified: Wed, 13 May 2026 19:13:34 GMT  
		Size: 2.8 MB (2835967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5232839e4c9b823f5a30e7d2f1e58cda5e34248ad9c94e3b8bda9c0d8066f0a2`  
		Last Modified: Wed, 13 May 2026 19:13:34 GMT  
		Size: 33.9 KB (33901 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:8f5b25553fe2d268244946131441bd37f8650d3f71d8f41018175b4e902f4cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67158092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c3051ce935848033aaf095b182e4483a8eb4de5f11e213e4f40b95861caf6b`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Wed, 13 May 2026 19:18:28 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:18:28 GMT
ENV NGINX_VERSION=1.30.1
# Wed, 13 May 2026 19:18:28 GMT
ENV NJS_VERSION=0.9.8
# Wed, 13 May 2026 19:18:28 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 13 May 2026 19:18:28 GMT
ENV ACME_VERSION=0.4.1
# Wed, 13 May 2026 19:18:28 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:18:28 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:18:28 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:18:29 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:18:29 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:18:29 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:18:29 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:18:30 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:18:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:18:30 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:18:30 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:18:30 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13c5dce2e6a798ce2a3293c2b1ec797ebf8ca4864e75516d6567075623fbcdcd`  
		Last Modified: Wed, 13 May 2026 19:18:51 GMT  
		Size: 33.6 MB (33555406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8acba367886b03febd93a7e9eca7d65d73846d88784ac5dd96238a8dcf95861`  
		Last Modified: Wed, 13 May 2026 19:18:49 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0479fadea87cf07a26d24dbb5224acb41d766dceeb18ec8c32ef3594216fb3ac`  
		Last Modified: Wed, 13 May 2026 19:18:49 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4e558a451068bdb27f345a6687d7393c56c27acf99934a1ee729b68134dff7`  
		Last Modified: Wed, 13 May 2026 19:18:50 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42ca154f2f4ab5881bfc6f5484e6aaaf5f0c08a3117c67a7aa6d1543008a848c`  
		Last Modified: Wed, 13 May 2026 19:18:51 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f18231727fb3bd6939ce0d69b1fc9521ed28f244fb9a045c27b9b1a4c8094e3`  
		Last Modified: Wed, 13 May 2026 19:18:51 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:4881efb3bbcaa413e95d55fcf107f383bcd4419f632e84fa763dddeb73287e04
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66cc26a82f97f069dbc3d04200dfb0aae7b38a0971c6cb66d84c940048aaa61f`

```dockerfile
```

-	Layers:
	-	`sha256:4597fc508e82ad1f04903c5835cfcc2f735a9e13df7466b5850bf7cd084d3dd9`  
		Last Modified: Wed, 13 May 2026 19:18:50 GMT  
		Size: 2.8 MB (2843617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6fbaeae5b1ed7b004c05fd4978d27ef446f9be4259d6c358aaf95c978096f5a5`  
		Last Modified: Wed, 13 May 2026 19:18:49 GMT  
		Size: 34.0 KB (33999 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:ea01760f3cdf6820401d9d0e4de0d8b2c188cb451032120e7e91e5850e62eaf9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57713513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:192bdc3399bf833295df1614879d54db895aa20fd7ba13eb452417054729e6b6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 09:39:36 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 14 May 2026 09:39:36 GMT
ENV NGINX_VERSION=1.30.1
# Thu, 14 May 2026 09:39:36 GMT
ENV NJS_VERSION=0.9.8
# Thu, 14 May 2026 09:39:36 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 14 May 2026 09:39:36 GMT
ENV ACME_VERSION=0.4.1
# Thu, 14 May 2026 09:39:36 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 14 May 2026 09:39:36 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 14 May 2026 09:39:36 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:39:37 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 May 2026 09:39:37 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:39:37 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:39:37 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:39:37 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 09:39:37 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 May 2026 09:39:37 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 09:39:37 GMT
STOPSIGNAL SIGQUIT
# Thu, 14 May 2026 09:39:37 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d81e6e73db27a2b4175e780f7d0a23c874b22fb4d7f377cdc0be7d3eba98e27`  
		Last Modified: Thu, 14 May 2026 09:41:08 GMT  
		Size: 29.4 MB (29428677 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b55fb779b8b01548ea43dba6f323497bc6039d5930284cd5eb47d7f3a63fc8bb`  
		Last Modified: Thu, 14 May 2026 09:41:03 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9b617fe6809befab2d787ac7121d0a4cc28eb093a78670f96fc85cd88bcb670`  
		Last Modified: Thu, 14 May 2026 09:41:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e96967a5f2e3c23652cd61b941413762c27c54ca5709df548a1b476d202f878`  
		Last Modified: Thu, 14 May 2026 09:41:03 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:247b0b29cd02ae7c5134fdce28e9b2eed899651a4a3c5c6e181d104fd97f8750`  
		Last Modified: Thu, 14 May 2026 09:41:04 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:309a2557d7e30847a056c6c750677d784eca3b75c0b188699eb6a4e2bd5350e7`  
		Last Modified: Thu, 14 May 2026 09:41:04 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:9dd1eb4f2cc87a25438e4f58ff2974865b72a86260fd1f582df7572f07f43003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafc1bfc793cfd1a52edf74367d43db56994a67409e03515d7b65df7821663ab`

```dockerfile
```

-	Layers:
	-	`sha256:4de49704885ccf2871e4634e422cdf6ee8894324683ffc48f3abdbb1ecd492ec`  
		Last Modified: Thu, 14 May 2026 09:41:04 GMT  
		Size: 2.8 MB (2833404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c9fd393d66cbfbce2750cb60598cad56bada0bba90ce040a417a2c79832dd896`  
		Last Modified: Thu, 14 May 2026 09:41:03 GMT  
		Size: 34.0 KB (33999 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:ae42a4b90ca5d6edcb645dc3cdecfbc00343f3bb0da76894dddae0a4c4d93804
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.6 MB (60588895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc8533c2a8ad97fd3e4961881533a2d3e3bb97cbcbfde0952fd3d287d8224b3f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Wed, 13 May 2026 19:10:36 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 13 May 2026 19:10:36 GMT
ENV NGINX_VERSION=1.30.1
# Wed, 13 May 2026 19:10:36 GMT
ENV NJS_VERSION=0.9.8
# Wed, 13 May 2026 19:10:36 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 13 May 2026 19:10:36 GMT
ENV ACME_VERSION=0.4.1
# Wed, 13 May 2026 19:10:36 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:10:36 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 13 May 2026 19:10:36 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="05e338105684bf659770c24af35264a25e6d02d4b850c3fb21091dd0815284ab567a0ae03a7756fb4ea94520a7a4057c1bd8967d62cf2fc4cf1fc11d424b56ba *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:10:36 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 13 May 2026 19:10:36 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:10:36 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:10:36 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:10:36 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 13 May 2026 19:10:36 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 13 May 2026 19:10:36 GMT
EXPOSE map[80/tcp:{}]
# Wed, 13 May 2026 19:10:36 GMT
STOPSIGNAL SIGQUIT
# Wed, 13 May 2026 19:10:36 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c93122c0fc6d9bf8102a0312c009af7314cf84afcf72249e29d5d6bdca0ebaf9`  
		Last Modified: Wed, 13 May 2026 19:10:51 GMT  
		Size: 30.7 MB (30743943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ea5aba192d7844cc339271350cd6112c88f203b24766c8809808205623161be`  
		Last Modified: Wed, 13 May 2026 19:10:50 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d88ac13f4b6eb873cd6992e7b1d74fb04105900366d0738b07de33bbefe529fc`  
		Last Modified: Wed, 13 May 2026 19:10:50 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce8fce603b6fde7d15b03ebe9d7446f8f8d206f97b02fa2b65dc7c8c28c4458`  
		Last Modified: Wed, 13 May 2026 19:10:50 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e48cf321d1e8f40d601fa3508c47f4f6a9b02f905017f719744122952f150d8`  
		Last Modified: Wed, 13 May 2026 19:10:51 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd5d842c2805b4b8e99931cd49fd87c193e207d8959d331b2669b757cb1b65f5`  
		Last Modified: Wed, 13 May 2026 19:10:51 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:eb206723713f71ac137d6ae383f30843a20844ba6588199ee2e643ac46122af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2783340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea2e35f990ffac86e61251201b88880c48c9dd911966500c4fa3ffec75a29af`

```dockerfile
```

-	Layers:
	-	`sha256:5e19b2c9f7adce9d4facad2510fa29a3155f3910148d87f99de38af3099f3c1c`  
		Last Modified: Wed, 13 May 2026 19:10:50 GMT  
		Size: 2.7 MB (2749397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fbb025ec990748ffc9d039087872766d9bfd92723240e1f41206f30fab50b65`  
		Last Modified: Wed, 13 May 2026 19:10:50 GMT  
		Size: 33.9 KB (33943 bytes)  
		MIME: application/vnd.in-toto+json
