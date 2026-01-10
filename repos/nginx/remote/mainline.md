## `nginx:mainline`

```console
$ docker pull nginx@sha256:7272239bd21472f311aa3e86a85fdca0f1ad648995f983ab6e5e7dea665cd233
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
$ docker pull nginx@sha256:c6c55d513dd0e897a6a1c1f1405e00f8fc49bf67eab2e14e43a705a9a6080b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62851539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e97da2b9cb35d218d73fefecde1e8c8864290bedc30ba54f8a817ddaaff6dd6`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:54:49 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 09 Jan 2026 18:54:49 GMT
ENV NGINX_VERSION=1.29.4
# Fri, 09 Jan 2026 18:54:49 GMT
ENV NJS_VERSION=0.9.4
# Fri, 09 Jan 2026 18:54:49 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:54:49 GMT
ENV ACME_VERSION=0.3.1
# Fri, 09 Jan 2026 18:54:49 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:54:49 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:54:49 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:49 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 09 Jan 2026 18:54:49 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:49 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:49 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:54:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 18:54:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 18:54:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:02d7611c4eae219af91448a4720bdba036575d3bc0356cfe12774af85daa6aff`  
		Last Modified: Mon, 29 Dec 2025 22:31:18 GMT  
		Size: 29.8 MB (29776533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5890669609837ed3eee730f13e0efda1c2beff95f6deaee315d742cbdb87288e`  
		Last Modified: Fri, 09 Jan 2026 18:55:10 GMT  
		Size: 33.1 MB (33070411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7674eff4effe22fe059b9dd1c9ab7098609c7c7774bdc640f5e8156031b7c416`  
		Last Modified: Fri, 09 Jan 2026 18:55:07 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e964620d7d020e94ce4abc4574e06d5af3c316be500614ab9120ce35522981d`  
		Last Modified: Fri, 09 Jan 2026 18:55:07 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24ca5634560a56b045bdb4884490b3fdc7fe0ee73c44ef77eba2b8659c8edde8`  
		Last Modified: Fri, 09 Jan 2026 18:55:07 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f0a5b0f1470e0895baed78183aa4b53f20a92174c02507714aa9c5f73e796c`  
		Last Modified: Fri, 09 Jan 2026 18:55:07 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964234ddf75fc14c5e5816398f396107c9166f1005a6a6de73ae822f2715b0be`  
		Last Modified: Fri, 09 Jan 2026 18:55:07 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:57314cd1fa693f5e7d35fab29e8fa93769d5f0278f0ba3bd3b77b9f91d5e4e82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852281 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b7f9cfb5283e83ce0ff08a917cac51cad1d29fe35fe330beeb1296f039dcd8`

```dockerfile
```

-	Layers:
	-	`sha256:61949c868b1ede697c707493636cee65385974fdad711fe8f660ffe4dde1a6f6`  
		Last Modified: Fri, 09 Jan 2026 21:50:41 GMT  
		Size: 2.8 MB (2817125 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6c17b65af2f575de83e9fb9284ede26c4761e024a6f55d467cebc9bee34b69d3`  
		Last Modified: Fri, 09 Jan 2026 21:50:42 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v5

```console
$ docker pull nginx@sha256:7a09dc2f8a99beaa0dea16c4df073775e4639e0d29b0c9169b2b28012f1ae5bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54078341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd18d4c3daacf2c20a3a94dd1e3982564c9a2730ea07394f75c6afed267f28d7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 19:03:02 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 09 Jan 2026 19:03:02 GMT
ENV NGINX_VERSION=1.29.4
# Fri, 09 Jan 2026 19:03:02 GMT
ENV NJS_VERSION=0.9.4
# Fri, 09 Jan 2026 19:03:02 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:03:02 GMT
ENV ACME_VERSION=0.3.1
# Fri, 09 Jan 2026 19:03:02 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:03:02 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:03:02 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:02 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 09 Jan 2026 19:03:02 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:02 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:02 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:02 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:02 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:03:02 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 19:03:02 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 19:03:02 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b99a8d8dab982a1a4ea341e66b178b14c0f373c2cd90ac46a67308a4f43c82ae`  
		Last Modified: Mon, 29 Dec 2025 22:27:09 GMT  
		Size: 27.9 MB (27944146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a21610e973326d5b7e4a81b0024966b17276986a3a9d17418862640b269315d3`  
		Last Modified: Fri, 09 Jan 2026 19:03:23 GMT  
		Size: 26.1 MB (26129589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc44e068642b798e36af3f7b39b6ac294aba34ad46fbc392c18ffd44dd08f0dd`  
		Last Modified: Fri, 09 Jan 2026 19:03:22 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6deb5cd4d892540c06922486c04ad8e9dd18e28c1bc6a8814f9dd5f73004dd9`  
		Last Modified: Fri, 09 Jan 2026 19:03:22 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7ab80be589509c61827db2a00dde0bd035d534ad85c049271044fe87b6bf997`  
		Last Modified: Fri, 09 Jan 2026 19:03:23 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41d33802e9ed0bbe73af5093fb027a57d3bb4882d3514a57f6e1186fa8e927d3`  
		Last Modified: Fri, 09 Jan 2026 19:03:23 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d42788f43df7e6355f2b8e874c0a2f4ab2ccad7b59e6c9006618ee56cfaa44c8`  
		Last Modified: Fri, 09 Jan 2026 19:03:23 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:c0be55ae96f80b1bb6f836e276161487d001c725fd0ccf6d968718e065302bb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2878549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25693deaf7c702d737bf905cb5a8e3fd96b57e7abbe3fa8454b6464e3358ab60`

```dockerfile
```

-	Layers:
	-	`sha256:2afcfe7d36e0b6e924dbce396b55152b925e8f947cb239b67cc870636a1a0762`  
		Last Modified: Fri, 09 Jan 2026 21:50:46 GMT  
		Size: 2.8 MB (2843265 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5014feb0bd1ff320fee02e5174e6bab77ffd576179795816d2a714870ec88a93`  
		Last Modified: Fri, 09 Jan 2026 21:50:47 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v7

```console
$ docker pull nginx@sha256:b22559a8caa9e9eb8b35e0c81933c6f03ea246f1c198d8bfa7f2e54acbf9c4de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52281384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19c6a32adbb90090f8589554c4512e4770443b42b4a9865138f0c7c5f33bb0b1`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 19:03:42 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 09 Jan 2026 19:03:42 GMT
ENV NGINX_VERSION=1.29.4
# Fri, 09 Jan 2026 19:03:42 GMT
ENV NJS_VERSION=0.9.4
# Fri, 09 Jan 2026 19:03:42 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:03:42 GMT
ENV ACME_VERSION=0.3.1
# Fri, 09 Jan 2026 19:03:42 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:03:42 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:03:42 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:42 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 09 Jan 2026 19:03:42 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:42 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:42 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:42 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:03:42 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:03:42 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 19:03:42 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 19:03:42 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:6d3e0fea3cb8eb29b9c06956265b47cd00f7ebfb48e35e818f686d52c21353f5`  
		Last Modified: Mon, 29 Dec 2025 22:28:07 GMT  
		Size: 26.2 MB (26210001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5db1582d26b29e20021f23b82dd031fa3de09fc61969677a3f8b820242b3d6`  
		Last Modified: Fri, 09 Jan 2026 19:04:01 GMT  
		Size: 26.1 MB (26066777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695cf14d191ea88a204d6b0b6768e98f714d32df12acbda4d0895602fce00554`  
		Last Modified: Fri, 09 Jan 2026 19:03:58 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7be60390512134a1856a53542f16f8629091d18986d6c32dd78142dfdbbab48`  
		Last Modified: Fri, 09 Jan 2026 19:03:58 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30d0cf47b54d41b98095f2404899a7e823c4989897a159534a2a0781ea411f53`  
		Last Modified: Fri, 09 Jan 2026 19:03:59 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842bd7ae1cd1d04410ac559c2a21acef5b99b8e5af8af3e66960d5fb5edc5d51`  
		Last Modified: Fri, 09 Jan 2026 19:04:02 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8269f0b9b7bb45a9f42f063bd84532fc492edab915a24cfaf438682ceb4ed3d0`  
		Last Modified: Fri, 09 Jan 2026 19:03:58 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:f11f65c7da8f2b521f3f5495f0c6cc5b16c04cb56fbf7c166acc9fa85be1a034
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cc5d8db961b853c15d98cbf23c2ba050dd0dab36767231976540335ae699b69`

```dockerfile
```

-	Layers:
	-	`sha256:3cae7b63bb2299705a56612cb6c60e3443bae2add950cdb301966b66fd6cf6dc`  
		Last Modified: Fri, 09 Jan 2026 21:50:51 GMT  
		Size: 2.8 MB (2842010 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f044b5814881b7e88d1b2c98d0f916dcdcb8f0041c036fb85093b850ccada3a9`  
		Last Modified: Fri, 09 Jan 2026 21:50:52 GMT  
		Size: 35.3 KB (35284 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:21e40209f956e650651f3326dfeaacda81e4c85c170d0cdcd0e0a684f4203dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61183539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a62506be47c03979d54f4d366b187c8885a2b47e5f46f0c10cb3909b39177648`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:54:21 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 09 Jan 2026 18:54:21 GMT
ENV NGINX_VERSION=1.29.4
# Fri, 09 Jan 2026 18:54:21 GMT
ENV NJS_VERSION=0.9.4
# Fri, 09 Jan 2026 18:54:21 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:54:21 GMT
ENV ACME_VERSION=0.3.1
# Fri, 09 Jan 2026 18:54:21 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:54:21 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:54:21 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:21 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 09 Jan 2026 18:54:21 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:21 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:21 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:21 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:54:21 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:54:21 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 18:54:21 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 18:54:21 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2ae15a20160209c6fd6cff4886e4ba2e666fa5bedd7b54a2c0097ea6646f0273`  
		Last Modified: Mon, 29 Dec 2025 22:31:09 GMT  
		Size: 30.1 MB (30138636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5de92b8645606ab6f1bfe9f439ce874a2e0e0e15ea336d5f9b55ff3ba719ace`  
		Last Modified: Fri, 09 Jan 2026 18:54:54 GMT  
		Size: 31.0 MB (31040307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca17c40d702a8eaa1949443be5a0700a2d02d9dad361809e03302273dd6cc5c4`  
		Last Modified: Fri, 09 Jan 2026 18:54:46 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e01b5e59ab491f4d979a01b27a690eaad863401e289f7997b2edcc44bf5bccad`  
		Last Modified: Fri, 09 Jan 2026 18:54:45 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eb534c72887f59a24499b57346f34c414b71d306e5ca3695369bb7f73e6fa8e`  
		Last Modified: Fri, 09 Jan 2026 18:54:45 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6f45d1635ffcc61bd20e62c5536079bbf46ff01ac0e64a6d454c1441f2ba817`  
		Last Modified: Fri, 09 Jan 2026 18:54:46 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d013df6a0cad34f753a51b5bd82617947ffadfe5cad35da5c877816a689414`  
		Last Modified: Fri, 09 Jan 2026 18:54:46 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:c0b5020d91ffcabc487629ce79bb7c016dd146f78ac6cf2bce412e2aae9cbfff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07d9d177fcac0d66a07fc55703d79168828e6645ce8e3bb1ae5e75a6d58500db`

```dockerfile
```

-	Layers:
	-	`sha256:16bef8ab06e1d6ac0659a7002a4c4df743df992399f27c1680605a46cbe067b6`  
		Last Modified: Fri, 09 Jan 2026 20:30:54 GMT  
		Size: 2.8 MB (2817609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d15cd9cf566eb1e9f38e656ee452692a3e3623fa5bed9c4f7e09224b247c96b6`  
		Last Modified: Fri, 09 Jan 2026 20:30:52 GMT  
		Size: 35.3 KB (35331 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; 386

```console
$ docker pull nginx@sha256:852fd8b4fb5a360ea934db4d84140caf4dc958da2ca95fac2879423172226425
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63245466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:161d1f998ece90764ff06e6a8cc93672783dc300d9c28b49c1580dfa2f246762`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 19:05:06 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 09 Jan 2026 19:05:06 GMT
ENV NGINX_VERSION=1.29.4
# Fri, 09 Jan 2026 19:05:06 GMT
ENV NJS_VERSION=0.9.4
# Fri, 09 Jan 2026 19:05:06 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:05:06 GMT
ENV ACME_VERSION=0.3.1
# Fri, 09 Jan 2026 19:05:06 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:05:06 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:05:06 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:05:07 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 09 Jan 2026 19:05:07 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:05:07 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:05:07 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:05:07 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:05:07 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:05:07 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 19:05:07 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 19:05:07 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:796ffff142a3158a5c48a8d81b8b722c5cf4889d5e22da70bdd13a6459d6e40b`  
		Last Modified: Mon, 29 Dec 2025 22:27:31 GMT  
		Size: 31.3 MB (31293100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfb64322c57a2c6365f9d96271ad92667f465bf574ebab356232bb6e54030593`  
		Last Modified: Fri, 09 Jan 2026 19:05:25 GMT  
		Size: 31.9 MB (31947762 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f987ba07d6fe41dd5ebb05799cc077d0a61e291536f85a920b27f7faf61b8e16`  
		Last Modified: Fri, 09 Jan 2026 19:05:22 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1c25d46405181e09c5014545fdddf93cbbba89ce2caec500b700283002716d9`  
		Last Modified: Fri, 09 Jan 2026 19:05:22 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4255a69d51bf5425f0f8b31cfd705b406bf6629366b8813406ced0e51f48313`  
		Last Modified: Fri, 09 Jan 2026 19:05:22 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b974529bf75145fd3c89c9c51ee69fe820db3f85df10fadba6afea021b40be0`  
		Last Modified: Fri, 09 Jan 2026 19:05:22 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67bb95ff5d806fe92cebadfad4d756b4810e8c16248478955c0caba0e8f2642d`  
		Last Modified: Fri, 09 Jan 2026 19:05:22 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:756eeb423a18f378ed656b780aabd9ec031c1a941a1853b7ab1dd962cf206015
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a412c498bf07608f3f469adf9d687b09d2cb7559b48965043b39880b6aec9a50`

```dockerfile
```

-	Layers:
	-	`sha256:9ec9cca975e23cce0536d82f3c3c38a30b05e4bf0a67c9214bcb4132009f85f5`  
		Last Modified: Fri, 09 Jan 2026 21:50:59 GMT  
		Size: 2.8 MB (2836961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed0cf74fcf1f932a02dd4a57c8d6e04d413f1da4f1fd78bcb3868e56dcb37f68`  
		Last Modified: Fri, 09 Jan 2026 21:50:59 GMT  
		Size: 35.1 KB (35093 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; ppc64le

```console
$ docker pull nginx@sha256:d13967df2acacedca16d9b1d69f6b5f3d924d1449ec9ff5acbd586d2adde392f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (66981339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9cf3a050bff954ac2bb1a357dc3545a42fb7bd5c1d430d83a86a0ccbb819d0bd`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 19:08:46 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 09 Jan 2026 19:08:46 GMT
ENV NGINX_VERSION=1.29.4
# Fri, 09 Jan 2026 19:08:46 GMT
ENV NJS_VERSION=0.9.4
# Fri, 09 Jan 2026 19:08:46 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:08:46 GMT
ENV ACME_VERSION=0.3.1
# Fri, 09 Jan 2026 19:08:46 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:08:46 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 19:08:46 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:08:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 09 Jan 2026 19:08:47 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:08:48 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:08:48 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:08:49 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 19:08:49 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Jan 2026 19:08:49 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 19:08:49 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 19:08:49 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:34b56ab3c5579c93222f3403d640c7a7f19044e9e46a2d1c6b1da60bde918efc`  
		Last Modified: Tue, 30 Dec 2025 15:11:02 GMT  
		Size: 33.6 MB (33596890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2f82b788f40e18cb041d9c5645999b58007f4d175253f7d9106529b7cd5aeda`  
		Last Modified: Fri, 09 Jan 2026 19:09:31 GMT  
		Size: 33.4 MB (33379854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b79afce3107055af1f20ff2a33e633484d38575af1d14a42c49ecc95c9763dd7`  
		Last Modified: Fri, 09 Jan 2026 19:09:26 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204922d58071d8626cef79f65a0613f0b3cc9448e251186eb682639cb14af162`  
		Last Modified: Fri, 09 Jan 2026 19:09:26 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f13ebf801b65e53a4f0e8151971eb1d4a7153cc98c7084ae331035e926a41f54`  
		Last Modified: Fri, 09 Jan 2026 19:09:26 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b01f153809c333e1e69403ddcf6c6779a11e023817cce10f8b8b3f1f5791321`  
		Last Modified: Fri, 09 Jan 2026 19:09:26 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7847681644e2351c1f7a1b82932d2b720b39cf728d97f7631439ad1f0b2b215`  
		Last Modified: Fri, 09 Jan 2026 19:09:26 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:d583169f6e72d217f51c623f248ccbe141409152e0992475541791bd5082bf77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2879891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3af225609878e231c37b9c6786050444693c9c911c6c31cee046ffcfe6420bd`

```dockerfile
```

-	Layers:
	-	`sha256:774f181643bb093e1fb896bd90bbc3df1a3757af7b0501d6a7a927c9a6a50477`  
		Last Modified: Fri, 09 Jan 2026 21:51:05 GMT  
		Size: 2.8 MB (2844655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:86663abb0d534165a564e2efb0253466be4c96599307354199db3ef419f9cc18`  
		Last Modified: Fri, 09 Jan 2026 21:51:05 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; riscv64

```console
$ docker pull nginx@sha256:453680c6c6708c469da72ac46819bdd11f7b7a4d4c0cfa3f274dee842b97c52e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57549055 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:513d0e593eeba31239ba5f8ffa0653c16bb0ff9fc152252ef21e920a7b009641`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1766966400'
# Sat, 10 Jan 2026 00:01:08 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Sat, 10 Jan 2026 00:01:08 GMT
ENV NGINX_VERSION=1.29.4
# Sat, 10 Jan 2026 00:01:08 GMT
ENV NJS_VERSION=0.9.4
# Sat, 10 Jan 2026 00:01:08 GMT
ENV NJS_RELEASE=1~trixie
# Sat, 10 Jan 2026 00:01:08 GMT
ENV ACME_VERSION=0.3.1
# Sat, 10 Jan 2026 00:01:08 GMT
ENV PKG_RELEASE=1~trixie
# Sat, 10 Jan 2026 00:01:08 GMT
ENV DYNPKG_RELEASE=1~trixie
# Sat, 10 Jan 2026 00:01:08 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Sat, 10 Jan 2026 00:01:08 GMT
COPY docker-entrypoint.sh / # buildkit
# Sat, 10 Jan 2026 00:01:08 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Sat, 10 Jan 2026 00:01:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Sat, 10 Jan 2026 00:01:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Sat, 10 Jan 2026 00:01:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Sat, 10 Jan 2026 00:01:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Sat, 10 Jan 2026 00:01:09 GMT
EXPOSE map[80/tcp:{}]
# Sat, 10 Jan 2026 00:01:09 GMT
STOPSIGNAL SIGQUIT
# Sat, 10 Jan 2026 00:01:09 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:96d8ad310358e2403b7b44cf38db606dc1ea6b58b915684d38e13f573860f64e`  
		Last Modified: Tue, 30 Dec 2025 00:53:22 GMT  
		Size: 28.3 MB (28273129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ac4083f3953eb21368fe61d4898635e6c2c885c5fe5c63aa51cac4d323979f`  
		Last Modified: Sat, 10 Jan 2026 00:02:49 GMT  
		Size: 29.3 MB (29271320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c1f6d0ce19b25db4bca22497caaf625274b286d4b542b7d8d3adb95f5708114`  
		Last Modified: Sat, 10 Jan 2026 00:02:48 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972de1df38d53284fce54fa68be105ae4e900b3ba3147443eba5a4a7d9aa27d5`  
		Last Modified: Sat, 10 Jan 2026 00:02:46 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:76ecfb7688fc81d83c478914ca5e6e8f4be64036614a369056bd28cb50eec049`  
		Last Modified: Sat, 10 Jan 2026 00:02:46 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:299525d281db9f9e1ac38246a7d49f1f770e94752c284adb008334d00e72d408`  
		Last Modified: Sat, 10 Jan 2026 00:02:46 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19797d0a92ef88ff3dba974fb804253980aaa20a1c83078a89fdea5b9e71dfe2`  
		Last Modified: Sat, 10 Jan 2026 00:02:46 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:65c524591a1eaa4191328b5a2f79307d23c82ae20cbe114ccb4e99b218b73f55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d84c3df5d98b0b472dd4bdc215942a482339f17fe0590f88f853a4247e63e63b`

```dockerfile
```

-	Layers:
	-	`sha256:be4cfed97027a56d5c7db3f5b5967c9964d7a23babb48258d39cd57a3031f227`  
		Last Modified: Sat, 10 Jan 2026 00:52:05 GMT  
		Size: 2.8 MB (2834442 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7eb546946f5db92b10ea3a05f5d10f8b416f6e82bff02b9f9afc87a4a7b432b2`  
		Last Modified: Sat, 10 Jan 2026 00:52:06 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; s390x

```console
$ docker pull nginx@sha256:d79e69b1ee7fdf264b3fbc37608abe431268be67b0e832502ff999f126b88433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60399562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a981c8f11b7c9d8aab6bd9059b91bd7f53d95606d84df7fde7ca6b69c1cb405c`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 29 Dec 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1766966400'
# Fri, 09 Jan 2026 18:59:58 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 09 Jan 2026 18:59:58 GMT
ENV NGINX_VERSION=1.29.4
# Fri, 09 Jan 2026 18:59:58 GMT
ENV NJS_VERSION=0.9.4
# Fri, 09 Jan 2026 18:59:58 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:59:58 GMT
ENV ACME_VERSION=0.3.1
# Fri, 09 Jan 2026 18:59:58 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:59:58 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 09 Jan 2026 18:59:58 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="e8b08060e10b8d8819e03533cb4922992ea138bcbf16a89a90593db719f17d78afa1cc4785592260c9c897753ec28c8b0d02c01df4b7d0e0ed286d0a42cef68c *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:59:58 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 09 Jan 2026 18:59:58 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:59:58 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:59:58 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:59:58 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 09 Jan 2026 18:59:58 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 09 Jan 2026 18:59:58 GMT
EXPOSE map[80/tcp:{}]
# Fri, 09 Jan 2026 18:59:58 GMT
STOPSIGNAL SIGQUIT
# Fri, 09 Jan 2026 18:59:58 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c9a83915f7d4b9d7fbe5dceeedd49718d2702fd67d78b63a38ec344f3fbfcc41`  
		Last Modified: Mon, 29 Dec 2025 22:27:07 GMT  
		Size: 29.8 MB (29834418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f67ec2eec45fee908b4ef93900159963db079f871afbb2cbe4a08602395c787`  
		Last Modified: Fri, 09 Jan 2026 19:00:28 GMT  
		Size: 30.6 MB (30560538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d997bbdf6f315b08ecdc2ce838091fe26c261da47d27c9fce8eec97557ae2417`  
		Last Modified: Fri, 09 Jan 2026 19:00:24 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e83a0f4ae5e60073a1e66cd53584f9393985209434d6e0beba3cee84fb8f075`  
		Last Modified: Fri, 09 Jan 2026 19:00:25 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22bed2d0c3f056f4a5eb271328a48eb3927736678fc2368c3097ff0dc3c326fe`  
		Last Modified: Fri, 09 Jan 2026 19:00:24 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3134f0652896376fa4f236c24ec452f2e8308ae5c2b1d77e7d1292609b63c91a`  
		Last Modified: Fri, 09 Jan 2026 19:00:25 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2442b2b990d4d77c56086a6b92247dad05d5a734985ef1212ed5c9119af0100e`  
		Last Modified: Fri, 09 Jan 2026 19:00:25 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:38699f05423d591ba72624905cbf1026c6674170f14ff99c064ebe06e706fc37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:586bb4a1b22b77d2e4a6e532012b3a39721014866ecbf742b94cb5950b41a945`

```dockerfile
```

-	Layers:
	-	`sha256:de7de3cf874c701caf9c5d44b4dfcc85a4c809f611f737872deeb38fad410e0b`  
		Last Modified: Fri, 09 Jan 2026 21:51:12 GMT  
		Size: 2.8 MB (2750411 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f900bea36198f2a04d4b7294f3afe85c8785493e9266000ac7620a5db586e20`  
		Last Modified: Fri, 09 Jan 2026 21:51:13 GMT  
		Size: 35.2 KB (35155 bytes)  
		MIME: application/vnd.in-toto+json
