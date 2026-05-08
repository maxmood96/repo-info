## `nginx:stable`

```console
$ docker pull nginx@sha256:50e2952b555d082947d1f70b190a6da1e731ba879116e238f4d1d5ade6b49b40
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

### `nginx:stable` - linux; amd64

```console
$ docker pull nginx@sha256:f9fe20134342dbdbf10b26abc7432e3e6f7a95141fdc5ad1722e2d4c8a883b09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62942598 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c4d33cb0a65f6fb7ba17e98256497511b2721e6255569bae0c5f0e11d89f38`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:22:51 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:22:51 GMT
ENV NGINX_VERSION=1.30.0
# Fri, 08 May 2026 19:22:51 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:22:51 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:51 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:22:51 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:51 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:22:51 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:51 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:22:51 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:51 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:51 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:51 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:22:51 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:22:51 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:22:51 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:22:51 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91c8c5cce4d1e05a6d929483e15daf42b329c898848ef6b8c3174ebf2a9dad9e`  
		Last Modified: Fri, 08 May 2026 19:23:01 GMT  
		Size: 33.2 MB (33157769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed16eb66f55deda2c0a97ee9a9b5ac2ac558703fc8ec657ba8588b24eecad28c`  
		Last Modified: Fri, 08 May 2026 19:23:00 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6aaf9472a1b82d346411d9e501136a1844018a94589a31db17a60bef4ed8b1c`  
		Last Modified: Fri, 08 May 2026 19:23:00 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebd30a3577a2e0a64a9449240356c667ede20a9f4082978a18ae7ac262f6de67`  
		Last Modified: Fri, 08 May 2026 19:23:00 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4077f6c0c7a1125e898216e3fc8f78b535d52ab3486e331dce22513f0648c7`  
		Last Modified: Fri, 08 May 2026 19:23:01 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9651dc0fec91a6da9fd799d22c6fa6a37d0ea848dd64b17efe04e651942c3d69`  
		Last Modified: Fri, 08 May 2026 19:23:01 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:7399f5691ed289ac0ddbc5150500cd3049f4543edc90fe1a6983f54748188234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2850054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:992d670ead771e6b9c06b64d8343ff3820118ae0e7acc214aa38ac6f767df263`

```dockerfile
```

-	Layers:
	-	`sha256:1a3f0d80d28e41296f2403c2c791f2b7b57020a9499ca1036c5e5877a70bc7f4`  
		Last Modified: Fri, 08 May 2026 19:23:00 GMT  
		Size: 2.8 MB (2816111 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:608b59253c0a957f6d91a33de398873fbac77a5ae6c5a816e925bd3a9aa38662`  
		Last Modified: Fri, 08 May 2026 19:23:00 GMT  
		Size: 33.9 KB (33943 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v5

```console
$ docker pull nginx@sha256:38700f44351208e3cab41023b4b8550d00d58b785f72fec27b4936b0c56c2033
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54152499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:483559c67ad9ac2a6a341e06df8aa4a869361487957139a65167e421229e7851`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:35:54 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 20:35:54 GMT
ENV NGINX_VERSION=1.30.0
# Fri, 08 May 2026 20:35:54 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 20:35:54 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:54 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 20:35:54 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:54 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:35:54 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:54 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 20:35:54 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:54 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:54 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:54 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:35:54 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:35:54 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:35:54 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 20:35:54 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70173682aef0200f48592b5542db617dab50e8910ca3942d5171228ceec2c7c7`  
		Last Modified: Fri, 08 May 2026 20:36:04 GMT  
		Size: 26.2 MB (26199695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4e626e7b2c923119348d1d4a3aafafe5904af03b1962d2212db2d8c9d00e34`  
		Last Modified: Fri, 08 May 2026 20:36:03 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26837c92b95a1bc0a5ebdad8d84911af810fd9eae60b669bfcc44d7aaaec1dc4`  
		Last Modified: Fri, 08 May 2026 20:36:03 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c4e6e9309a0c9628655fee0e84f907276510a3007734ce3ee4dc6c4e040dc48`  
		Last Modified: Fri, 08 May 2026 20:36:03 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a59adba3b099e4cd569f0d5d7c30258abe70bcf6d276f2a43fafb83466d5d9c`  
		Last Modified: Fri, 08 May 2026 20:36:04 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56577029d811e1878ec83aeeefdad2a4b0d46f13b4999e04e0dfd371f9d1376f`  
		Last Modified: Fri, 08 May 2026 20:36:04 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:b95db7acc4c482ec49b66949e395f7c89fda5aaad4318842507431f6256dfb52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2876258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8632ffc7e3d52575cbfe0e54156d7912feb0c1bc7b5739e6d0f61be08b3a742e`

```dockerfile
```

-	Layers:
	-	`sha256:ca2fe01279fac4852bc98ccd5a78d7810f1e1a8c8eb9a8def6a4024d9989b160`  
		Last Modified: Fri, 08 May 2026 20:36:03 GMT  
		Size: 2.8 MB (2842219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4734b270124f05633615e32794e3380eeede2848418b7377283b04865f877ad`  
		Last Modified: Fri, 08 May 2026 20:36:03 GMT  
		Size: 34.0 KB (34039 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm variant v7

```console
$ docker pull nginx@sha256:c97eda2fa74b137f7239d086cefd502db812955b0b85c256cefae5f8015fa30f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52361343 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a00041d10fe5caa8d12794ca0b1a02bdfdfe44e55962739e5d4501daeb4205d`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:24:24 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:24:24 GMT
ENV NGINX_VERSION=1.30.0
# Fri, 08 May 2026 19:24:24 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:24:24 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:24 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:24:24 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:24 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:24 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:24 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:24:24 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:24 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:24 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:24 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:24 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:24 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:24:24 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:24:24 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75161b22be6f6404710a12dea07fee767aee99dd176ef545a54966df2807d352`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 26.1 MB (26141829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8c4c7e1c86c7d36ac720583a7826ccfa59e9f2ffbcb80d237740bae2f7ab454`  
		Last Modified: Fri, 08 May 2026 19:24:33 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ce7e67f41132647f187d14a16b57d89f907ccfbebaa5a6bc586f161a33abde`  
		Last Modified: Fri, 08 May 2026 19:24:33 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57360efc10745550578c39888c7fc4380db1b7971b84f2f3797042c355c02142`  
		Last Modified: Fri, 08 May 2026 19:24:33 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a31690c60dc18433cab2d5ecfa47e4eda0ed5eb2fd641adfcd8682fcd5261d42`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41514f99d39bf6d95d8c2db8ec519b1a679b90a22eca0bd7b77765810296215c`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:e7157438b0344cd95e0d3557f7bfb876a7238d61a86d082c5c9587f26158adb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2875003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8be7e4be4e9aa775bf13ea820edf02094f45056ed6033f49321826392f22d4b6`

```dockerfile
```

-	Layers:
	-	`sha256:66b5b40c4922c1ed5ce1f66c4ba32afc4cf846c8f6188277e3ca63c43ce65564`  
		Last Modified: Fri, 08 May 2026 19:24:33 GMT  
		Size: 2.8 MB (2840964 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:186207b1390bf3e467e64f298bfcf7f84e838db6d586c7d101707d202160c78e`  
		Last Modified: Fri, 08 May 2026 19:24:34 GMT  
		Size: 34.0 KB (34039 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:75ad10f0ced98ec0ca4fabf753732d625b453e0c82a814b12c7eb0c769cb9010
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.3 MB (61288464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:603c651b91ddee0ff6f66e1a4533149bcaa8ef1e2cca84e13b83365a451b02c5`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:21:47 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:21:47 GMT
ENV NGINX_VERSION=1.30.0
# Fri, 08 May 2026 19:21:47 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:21:47 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:47 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:21:47 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:47 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:21:47 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:47 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:21:47 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:47 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:47 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:47 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:21:47 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:21:47 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:21:47 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:21:47 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:825ea360631f46f25e756f11d3e128980519fb4c669b81cc00475d7170242949`  
		Last Modified: Fri, 08 May 2026 19:21:57 GMT  
		Size: 31.1 MB (31140220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf14d9c716a54271c070b25287f1e3af7699f93e2b9f29fd851388d3ce6bb0a7`  
		Last Modified: Fri, 08 May 2026 19:21:56 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b168e97c71d522e9503290ee2e620a365dbd1b7d9fb22cf982bccea15da792c7`  
		Last Modified: Fri, 08 May 2026 19:21:56 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a68a77e211399b33ca0c73c4c186e2a5fffa5a67efbaddcbc01b5b54d9b50e`  
		Last Modified: Fri, 08 May 2026 19:21:56 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:076f36c2c8fa2a3daf795cfcb68397cae9a2e73634eb3fcbb6c49ebe384f40e9`  
		Last Modified: Fri, 08 May 2026 19:21:57 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59f01100b83c5933ff037040cda7aa049e5ed99887fc04329b9f231a3761c511`  
		Last Modified: Fri, 08 May 2026 19:21:57 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:7fc8b3802501b73dc382ebf2bb0b38ad8b8c8edb6ebb6233b20cb3d5dbd2b9f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2850618 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dd4052b4fa136a7070c50e9f8c2a2902fc556a300587d2a6ed8ae5f7312645a`

```dockerfile
```

-	Layers:
	-	`sha256:d3753e84564e3dab363dbf54ebc26431b800d8ee3fd42918941121ca21d40bdf`  
		Last Modified: Fri, 08 May 2026 19:21:56 GMT  
		Size: 2.8 MB (2816547 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1c3739925c68d6bb85211e612289138f26a4c7093f24a23dd0995b318c688865`  
		Last Modified: Fri, 08 May 2026 19:21:56 GMT  
		Size: 34.1 KB (34071 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; 386

```console
$ docker pull nginx@sha256:5f977a9e8168681d391f5774d8d537e1fea40a6884f4ab6e391042723fbbfbb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63327099 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c878a04444dc551bc5a12f46a64268b109ff6bc9a833be77cd8e8a7f91c1e6e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:24:27 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:24:27 GMT
ENV NGINX_VERSION=1.30.0
# Fri, 08 May 2026 19:24:27 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:24:27 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:27 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:24:27 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:27 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:24:27 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:27 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:24:27 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:27 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:27 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:27 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:24:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:24:27 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:24:27 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:24:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae28689fa4d9a6a8a981c263bd25502c9afcffda86d62b7749e7f5f7c925bd38`  
		Last Modified: Fri, 08 May 2026 19:24:38 GMT  
		Size: 32.0 MB (32026094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5dbb0386253c6d43b6b08847de2ad10d0911db67ebae672f2ce6cf31b9051a43`  
		Last Modified: Fri, 08 May 2026 19:24:36 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04447e6d8270a5260f4bfae7a2b97130a42511ebea14669dbb630bd6c88b2e5`  
		Last Modified: Fri, 08 May 2026 19:24:37 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1892c842d834f24e7ada4dabf6014d5c49905db66024c57400af392c836ca5fe`  
		Last Modified: Fri, 08 May 2026 19:24:37 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75b2e106ab5f50fc2fee2b71273a79327e12b9bfe9d8d00e0b7e78c35923fdf2`  
		Last Modified: Fri, 08 May 2026 19:24:38 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dfec9eaeac58418e839ea038c64e2845979708b56e9c90adafa21cb2ddbcd4`  
		Last Modified: Fri, 08 May 2026 19:24:38 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:842af363670fbf21ec9f8950c5bb2c0c35f3d174fe4c611804396433efcde8a6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2706d230895156c85f5f68f187205cf09f7755a639482d76f85cef8f672b167f`

```dockerfile
```

-	Layers:
	-	`sha256:a72eb0770dc3930348d1fb5726d41823a9348958fb1a83aeb555ff12a1b17dc2`  
		Last Modified: Fri, 08 May 2026 19:24:37 GMT  
		Size: 2.8 MB (2835967 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ff58d834c3523e6991add9854e9f36f5d920fe173f84a5bf8eee54f85690c95`  
		Last Modified: Fri, 08 May 2026 19:24:36 GMT  
		Size: 33.9 KB (33901 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; ppc64le

```console
$ docker pull nginx@sha256:fc7b389c8297d1e5f3e85e12e43580a9d053c0c3ccc51d14bebaf2577aff802b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67085796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebe0ee795f314e73b95122cc45d371795dc1fdfbcc3d36e27bbea30a8f592ecb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 20:51:31 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 20:51:31 GMT
ENV NGINX_VERSION=1.30.0
# Fri, 08 May 2026 20:51:31 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 20:51:31 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 20:51:31 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 20:51:31 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:51:31 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 20:51:31 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:51:31 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 20:51:32 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:51:32 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:51:32 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:51:32 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 20:51:32 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 20:51:32 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 20:51:32 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 20:51:32 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:552e4b0c1c9d2c3707f093367bf175ce5042e4e7ace32af397aa7efe87cb3c5f`  
		Last Modified: Fri, 08 May 2026 20:51:52 GMT  
		Size: 33.5 MB (33483105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:692feaa11c5baf4a5848534aa42475f30777d5442ac34fe660a90a959b44e932`  
		Last Modified: Fri, 08 May 2026 20:51:50 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:343364d188ac0761e952c0ea8c7012ea1c3852cd0d2884ab4dd229ba53aaebc3`  
		Last Modified: Fri, 08 May 2026 20:51:50 GMT  
		Size: 959.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4feaddb11c1a4e4cf98943cfba86d20524d274cb704dcff29701dde1f4e40831`  
		Last Modified: Fri, 08 May 2026 20:51:51 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79f40c8165103064dab53502c51f6d123014a6f4fd3463bf6c5c9227eb0eac62`  
		Last Modified: Fri, 08 May 2026 20:51:51 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2956d89f4cbcb4b6ecdc14e35c0c71741c9ca25c0db3ca38924b70fcc933db0`  
		Last Modified: Fri, 08 May 2026 20:51:51 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:81d58e79cf35c374846ebfbb76199efcd313c6a82b211dcb35aaf8103521afbc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56b14a159df6df7cd26eb011c08e12046f0750c7a4d86b64ce845078f0546a16`

```dockerfile
```

-	Layers:
	-	`sha256:9907026c899ab20d8255e1ffc873789ab3827a30e3f463c01293c7858575230a`  
		Last Modified: Fri, 08 May 2026 20:51:50 GMT  
		Size: 2.8 MB (2843617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8264cb76e3ae5ba475b3c870645cc60f1f5ba19ca88302b0c61a536d5ab10987`  
		Last Modified: Fri, 08 May 2026 20:51:50 GMT  
		Size: 34.0 KB (33998 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; riscv64

```console
$ docker pull nginx@sha256:5f162a9d9ad1054bf158dcaf8a8a69e140798741e5b41d914833ec13b755a8c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57653062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf246dfffeccb2a635805ab9b1104fec05c3e8957b287a2696d299e7ab8d766a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 14:26:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 22 Apr 2026 14:26:05 GMT
ENV NGINX_VERSION=1.30.0
# Wed, 22 Apr 2026 14:26:05 GMT
ENV NJS_VERSION=0.9.6
# Wed, 22 Apr 2026 14:26:05 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 22 Apr 2026 14:26:05 GMT
ENV ACME_VERSION=0.3.1
# Wed, 22 Apr 2026 14:26:05 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 22 Apr 2026 14:26:05 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 22 Apr 2026 14:26:05 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 14:26:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 22 Apr 2026 14:26:05 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 14:26:05 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 14:26:05 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 14:26:05 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 22 Apr 2026 14:26:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 22 Apr 2026 14:26:05 GMT
EXPOSE map[80/tcp:{}]
# Wed, 22 Apr 2026 14:26:05 GMT
STOPSIGNAL SIGQUIT
# Wed, 22 Apr 2026 14:26:05 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:c59e3a1f334be9f0528643dd07d69319f75f877f83be33ec1eff872a489985a0`  
		Last Modified: Wed, 22 Apr 2026 02:30:51 GMT  
		Size: 28.3 MB (28280195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f94508873f92c70e9190daef739b27d59db98b76ba5ef3193a68ac1d0d93ad`  
		Last Modified: Wed, 22 Apr 2026 14:27:36 GMT  
		Size: 29.4 MB (29368262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc738cd43ef13f9997725394ca21922c44379285b3cbae343fbc785d64e3d59c`  
		Last Modified: Wed, 22 Apr 2026 14:27:31 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a3eb5eb38d6f1c2c25e7fb2ff3c3066eda2d76b3101a0c3be6ff63bdbc9550`  
		Last Modified: Wed, 22 Apr 2026 14:27:31 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89343eccdfdc3490eecec0f46bf32c4d75f6b800e29ae6546a94be259b775102`  
		Last Modified: Wed, 22 Apr 2026 14:27:31 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2d08c6b4d253d9ffcb8eb19f721e7974a60df5934eb2e6ae4b029b11cc4a015`  
		Last Modified: Wed, 22 Apr 2026 14:27:32 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43601b298d4e59e61942699cb0bd660a2f94a4e6218ded327110c0774abe7c33`  
		Last Modified: Wed, 22 Apr 2026 14:27:33 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:a55cec09ac3cf59b59807dab21fc3e4b9e36e015ff75e11b66a0973f2ad45e22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2867402 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:257e153ea69f20658256e8598365cd83269ac3fcd12385404ea95bc014c4e2d7`

```dockerfile
```

-	Layers:
	-	`sha256:5efb0b6dfcbf8ed809828bcf22b4d3b6b67172b9beff497a46d2a1de9e89bd5f`  
		Last Modified: Wed, 22 Apr 2026 14:27:32 GMT  
		Size: 2.8 MB (2833404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9267b8d07fc4f7e1fedad4b44da86704f8d7e274557db61c9ac2867e5115807`  
		Last Modified: Wed, 22 Apr 2026 14:27:31 GMT  
		Size: 34.0 KB (33998 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:stable` - linux; s390x

```console
$ docker pull nginx@sha256:a5a309e087b0468dac60f04b2d98e1f53ff8f9b9e476fa49dfb4af87f2293424
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.5 MB (60498683 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b523f9bd1a22ba1e43c4baa5318f7c6fb52d18ede712fa0168fe4795e5ee0341`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Fri, 08 May 2026 19:28:44 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Fri, 08 May 2026 19:28:44 GMT
ENV NGINX_VERSION=1.30.0
# Fri, 08 May 2026 19:28:44 GMT
ENV NJS_VERSION=0.9.6
# Fri, 08 May 2026 19:28:44 GMT
ENV NJS_RELEASE=1~trixie
# Fri, 08 May 2026 19:28:44 GMT
ENV ACME_VERSION=0.3.1
# Fri, 08 May 2026 19:28:44 GMT
ENV PKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:28:44 GMT
ENV DYNPKG_RELEASE=1~trixie
# Fri, 08 May 2026 19:28:44 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="a090f4aecd628ab4b4124376efa55f617a272f9bae4e306df9b659b1b850133b0806cac31fb2a72faf1cc36bde8f5a19f4f5da5fd73502d3bbe374697920344e *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:28:44 GMT
COPY docker-entrypoint.sh / # buildkit
# Fri, 08 May 2026 19:28:44 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:28:44 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:28:44 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:28:44 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Fri, 08 May 2026 19:28:44 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Fri, 08 May 2026 19:28:44 GMT
EXPOSE map[80/tcp:{}]
# Fri, 08 May 2026 19:28:44 GMT
STOPSIGNAL SIGQUIT
# Fri, 08 May 2026 19:28:44 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed911604c16d1ab65f741bbfb402991ddad69cac10209092d97aa2ac0221db1b`  
		Last Modified: Fri, 08 May 2026 19:29:00 GMT  
		Size: 30.7 MB (30653730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:941c1133a18a996ab491bd7bc0c5ddeada2f63b8b594d3cdd5233c80f8c3a61e`  
		Last Modified: Fri, 08 May 2026 19:28:59 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8511700030ab3bf0f70a5d7acd032ac09eca64d2dde8160a1639dac841dda532`  
		Last Modified: Fri, 08 May 2026 19:28:59 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4e6c27f1c1a4d78b6a438ea24bfcc2381f542f87d2851a172e9811d46d54696`  
		Last Modified: Fri, 08 May 2026 19:28:59 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c8d5d5feca4120c085f386a95a9a11fff7d35f7b1ec1b0965f16080a768492d`  
		Last Modified: Fri, 08 May 2026 19:29:00 GMT  
		Size: 1.2 KB (1213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497f91cba29f010773597d0b65c6b826e381b1f7ec85b4372f4d8e3b6361f463`  
		Last Modified: Fri, 08 May 2026 19:29:00 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:stable` - unknown; unknown

```console
$ docker pull nginx@sha256:b39c1b8bda0e7368bb064c5f23e34194d34ebe0561f5b2fc6ef7ed860822c39c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2783339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0323e8fa57a4f96b43442a18442a54a7b4cc56ec76ff3be389940fdc9b8d035`

```dockerfile
```

-	Layers:
	-	`sha256:e573a0746aa11094ccd25cbc0c143af7be1f7ef565e62cce83c4ded5c193a99c`  
		Last Modified: Fri, 08 May 2026 19:29:00 GMT  
		Size: 2.7 MB (2749397 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8618f300f28905a60bc024aa07bf376cdcb0cf4760f608839ffd78c7ca188f3b`  
		Last Modified: Fri, 08 May 2026 19:28:59 GMT  
		Size: 33.9 KB (33942 bytes)  
		MIME: application/vnd.in-toto+json
