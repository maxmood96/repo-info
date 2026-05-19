## `nginx:mainline-trixie`

```console
$ docker pull nginx@sha256:f923b3e6cde4d9e6bd1894cc8bbe00853ac6ce48f48bd1372e8edd63bb7a832d
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
$ docker pull nginx@sha256:7d7a239e91eeeb6a94e16ab0abd3ed01660683d8d7114501d14318c0572b9479
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66054600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:278167866016613f0e0e2d57af00994c8b83df152fe0b15daf7d0ae75b643860`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 20:14:18 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:14:18 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:14:18 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 20:14:18 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 19 May 2026 20:14:18 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 20:14:18 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:14:18 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:14:18 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="9d879d57ef75661eaed35e787ef434b2f85771f6"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:18 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:14:18 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:18 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:18 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:18 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:14:18 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:14:18 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:14:18 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:14:18 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:57fb71246055257a374deb7564ceca10f43c2352572b501efc08add5d24ebb61`  
		Last Modified: Fri, 08 May 2026 18:24:13 GMT  
		Size: 29.8 MB (29780226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c788c06aafadbb741681ffd43c075edd4228bc7bf9a490ee506c19eeca6e9134`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 36.3 MB (36269780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24f607c25174ce68feedb5f87eb42469c634265d24bfb46fac126ff10b83c42c`  
		Last Modified: Tue, 19 May 2026 20:14:28 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:623d22e40ab847b9d9ca6f8e70e664357fc40662b1e824b8716f026be987eaf1`  
		Last Modified: Tue, 19 May 2026 20:14:28 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d34fde8cba255416400ddb54ed723c7c40c3284999af9a9b541e742c8a35507`  
		Last Modified: Tue, 19 May 2026 20:14:29 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1edf3f2b38ff281a887854037d33364b109e786cd27efcbb8b16cf3d1c6fe3a2`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4e94facf22dc6f2c2f0bc6d7ee29dd15812d98c6d2981105f5e2610bf43f909`  
		Last Modified: Tue, 19 May 2026 20:14:30 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:4297944152753b97c667420360a26312d0a765c684a2e573800a2dacce90bbc4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852510 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adf6f78c3c9c33274b89ae2543db0df2452cacb22ea922b549fabc36b8e5ad96`

```dockerfile
```

-	Layers:
	-	`sha256:72e962f0a02d3c10c97b973b08933888b68835e015ad9f85553886c6bbc3898a`  
		Last Modified: Tue, 19 May 2026 20:14:29 GMT  
		Size: 2.8 MB (2817333 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fae7a8121d0f406e5cc2eb9e0f0f4720d523d57466a42be62853f4c8d943c9c4`  
		Last Modified: Tue, 19 May 2026 20:14:29 GMT  
		Size: 35.2 KB (35177 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm variant v5

```console
$ docker pull nginx@sha256:65f53183886e841fb9dbc0b63d063123838bbea6a7640a391098c5ea0b4197d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62305944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db5bd9e7f345f86adae2c441a560aabafa03cb17d12c103c72822824855f7dd8`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 20:24:34 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:24:34 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:24:34 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 20:24:34 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 19 May 2026 20:24:34 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 20:24:34 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:24:34 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:24:34 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="9d879d57ef75661eaed35e787ef434b2f85771f6"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:24:34 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:24:34 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:24:35 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:24:35 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:24:35 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:24:35 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:24:35 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:24:35 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:24:35 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:8f774e9b92b540806fc05167db7ce09a3e1b12abdb9d496f7b8c82138656065a`  
		Last Modified: Fri, 08 May 2026 18:33:49 GMT  
		Size: 27.9 MB (27948200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2154e4227156f6f9ed46899492e4f2e01dc686dd5ee1609014afe2757c4b817`  
		Last Modified: Tue, 19 May 2026 20:24:46 GMT  
		Size: 34.4 MB (34353144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a5e941f420668aee334c86a0941c7a2e2a1aae59e2f21e42ae96677fc12c885`  
		Last Modified: Tue, 19 May 2026 20:24:44 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:858623af0aab591522f5530dc095d238821ced8fd4b438b660433f8fad1b93f4`  
		Last Modified: Tue, 19 May 2026 20:24:44 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e83393997a7fe1799f54e2463957d3717061a95deb5154e2600ed61f460a870d`  
		Last Modified: Tue, 19 May 2026 20:24:44 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca1f5b95405a1dbd990112e81d00e7a6ce87225fb168eda140ed970aba7f8b0`  
		Last Modified: Tue, 19 May 2026 20:24:45 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6c772e2b8608c93d70959ec6c354a0355817865292245483185c8fdc38bd734`  
		Last Modified: Tue, 19 May 2026 20:24:46 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:cbae4ab5a6cc0688034c45e15cd7bc6f0b939069e03a99ccf8bb08ce9ed7e999
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2878778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73aa639ff2aad53458e70e3c19ca0863990beaf353fd9601601390a9e7111182`

```dockerfile
```

-	Layers:
	-	`sha256:62903e18c3da97fcb4f85b6f15e092cbfbc185c54c1fbab2f4e902a4f6ac9573`  
		Last Modified: Tue, 19 May 2026 20:24:45 GMT  
		Size: 2.8 MB (2843473 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f37a470368dca25f060e7e7bb3d7524c232baddfa87edc63c8a582a9d162471`  
		Last Modified: Tue, 19 May 2026 20:24:44 GMT  
		Size: 35.3 KB (35305 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm variant v7

```console
$ docker pull nginx@sha256:956d89102181e43b140f4e8578d3149f68af9f1eae1d30e70fed8e38364029d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.0 MB (59979686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6dfb10d4a6b17d183abfae7204ddab404c7f20961998541f0ea4ddaff00e624`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 20:22:30 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:22:30 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:22:30 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 20:22:30 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:30 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 20:22:30 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:30 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:30 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="9d879d57ef75661eaed35e787ef434b2f85771f6"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:30 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:22:30 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:30 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:30 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:30 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:30 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:22:30 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:22:30 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:22:30 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f1433620eadfdfe016c8054b954f619ae5bca159f35a9459c36a76d9ef4d39c3`  
		Last Modified: Fri, 08 May 2026 18:37:58 GMT  
		Size: 26.2 MB (26214912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ade9ecb52fe781318103125651e16810c2f83e522ece518e126137b9be8843bd`  
		Last Modified: Tue, 19 May 2026 20:22:41 GMT  
		Size: 33.8 MB (33760172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ceb9685b19e1b78b990034ab3cdafadd2900f15ef20d98d4973afb10b4bffad`  
		Last Modified: Tue, 19 May 2026 20:14:50 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4c4d5689fd042918030d03dd9322d9789b9e1856dbc5216c88fe481caa8c96c`  
		Last Modified: Tue, 19 May 2026 20:22:40 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba06000728a859ecbe14b5e199b8f33959d4ffc800942958518e4d7cdc27c999`  
		Last Modified: Tue, 19 May 2026 20:22:40 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8ada33f20db0d046f4770d3d5be2ff2f7388f700c4aa52345304daac712f93`  
		Last Modified: Tue, 19 May 2026 20:22:41 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da13b7e0289747e880fc812b062965ac8448f71a1be10c17b6f1a39d31f1a23b`  
		Last Modified: Tue, 19 May 2026 20:22:41 GMT  
		Size: 1.4 KB (1398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:bba9e5b7b3769528df7aff269f3fab8084752bf01477c94a3632360eddd240c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2877523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1eac3b1b4cf8400377e7fc302ec9d778a59fee4b4a972899c5bfec10f4605f8`

```dockerfile
```

-	Layers:
	-	`sha256:8eb73a90f25d17cf9cf8b07ff6b0447ab6eea6d6c2bd9f875e12aa561c616c28`  
		Last Modified: Tue, 19 May 2026 20:22:40 GMT  
		Size: 2.8 MB (2842218 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4bd533ba28bdd52cf03f45c60ef0414dd3063e8ff4c1843c01366c1c6ec7a35`  
		Last Modified: Tue, 19 May 2026 20:22:40 GMT  
		Size: 35.3 KB (35305 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:22a9ca3229dda6d35d4c778e164946f2c84b28e088588921370bf7455f4201a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64719288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f5032e6f46be64e9bd28ab2d424656339d52a6718afa8e8e89f240a8f2b53476`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 20:13:01 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:13:01 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:13:01 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 20:13:01 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 19 May 2026 20:13:01 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 20:13:01 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:13:01 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:13:01 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="9d879d57ef75661eaed35e787ef434b2f85771f6"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:01 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:13:01 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:01 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:01 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:01 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:13:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:13:01 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:13:01 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:13:01 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:9ebf9a1d0c9ca1bcb377e9dba38a3fdd3e89cf37164f4245286c24f8cd50a39e`  
		Last Modified: Fri, 08 May 2026 18:26:50 GMT  
		Size: 30.1 MB (30143642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d9650a255f97627dfd40f8ebfa5deca50c91d7fa27338b34122d01db13c6234`  
		Last Modified: Tue, 19 May 2026 20:13:12 GMT  
		Size: 34.6 MB (34571057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b86a679a74e745c7d8324ca7ef939c58b39d72edaf89e1973e96643d990ca17d`  
		Last Modified: Tue, 19 May 2026 20:13:11 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a106e0606e027d6b5cda839126464c97b108f40021d0bea63aa4bea5f0745bb6`  
		Last Modified: Tue, 19 May 2026 20:13:11 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:101c1dcd7bb26c93f501aeb1639fd44317e397b798acc15fb6f848b86e611ba3`  
		Last Modified: Tue, 19 May 2026 20:13:11 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17aadcb08529d7a81a47ba7024af1123e4888a2561e704f1cf6e99d1775eea93`  
		Last Modified: Tue, 19 May 2026 20:13:12 GMT  
		Size: 1.2 KB (1207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b85bae9288d1a97a4d082ede23ff6e3b7462706ed8e9b951155e78fad7e921ee`  
		Last Modified: Tue, 19 May 2026 20:13:12 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:9b74f9ea240d2013ee5b5324f515675573ad8e4cfe47b7925557cf67f8f90a06
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f57456cc1fa675f66345082a5a7a7c74c92529bc4cf2b3e9f5ae0f37a75a7103`

```dockerfile
```

-	Layers:
	-	`sha256:7fad28aaa83dc5ce7d0f82124a1dc14d652f4e2f68d3329cfe14f148ab6928de`  
		Last Modified: Tue, 19 May 2026 20:13:11 GMT  
		Size: 2.8 MB (2817817 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d2c9a08897d25b5d5bf5121fd5b1194704cc93362194a937b156399d599ab18`  
		Last Modified: Tue, 19 May 2026 20:13:11 GMT  
		Size: 35.4 KB (35353 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; 386

```console
$ docker pull nginx@sha256:9fec82da26699b5c3dd8f312e0887c7a71ce0883906c9e8f05bd762a62774ab8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71882630 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aafefffd8e5eebd0fbe0306acca640102009376a7fd8783aaf49206835cbceab`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 20:22:05 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:22:05 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:22:05 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 20:22:05 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:05 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 20:22:05 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:05 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:05 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="9d879d57ef75661eaed35e787ef434b2f85771f6"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:05 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:22:05 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:05 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:05 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:05 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:05 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:22:05 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:22:05 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:22:05 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:43e2ffbaa23260ffb4e3de716920f2ed9e6af56e465ca1233a2d84c2cc1cf005`  
		Last Modified: Fri, 08 May 2026 18:32:48 GMT  
		Size: 31.3 MB (31296400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e65514493809fa2cb1d552460eacd9d2838aa666094e826aa1890b75f43a89`  
		Last Modified: Tue, 19 May 2026 20:22:18 GMT  
		Size: 40.6 MB (40581640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64fa04258a6275e8673aa1a226aaaa40f944bd614f53fde4694b8bf7a54c1c45`  
		Last Modified: Tue, 19 May 2026 20:22:16 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e76369f6606ab7a2fb7f835df5e9ec989be7ea8a04e0ad069eba369d2e76694c`  
		Last Modified: Tue, 19 May 2026 20:22:15 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89081a4cacee8912b643f425bec82e2a52ba5e07cc22ba2dbcd44dcda699297f`  
		Last Modified: Tue, 19 May 2026 20:22:16 GMT  
		Size: 404.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3db907117efbf44c91758bf7bb0a816463777df55828602f53399b180eb36bf`  
		Last Modified: Tue, 19 May 2026 20:22:17 GMT  
		Size: 1.2 KB (1209 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eac1eeb2a321d76f671b5d1f3c422c0f4426998fc6fd5c13f9f91f58bb719894`  
		Last Modified: Tue, 19 May 2026 20:22:17 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:320083e5e4048eb89e2909f083e8355f3f5839cba34ff64ba8f07faacc5970c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:affaab9fc66ffefe3e7013201c46b4781199445865f39281f08f051bc647a771`

```dockerfile
```

-	Layers:
	-	`sha256:b16017d97faa7400c88ca8ef0217483ed0429d26ffed1bcd8968c6c267386cc2`  
		Last Modified: Tue, 19 May 2026 20:22:16 GMT  
		Size: 2.8 MB (2837169 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8654dd55521d44b1b0605dca5211cde58ab640d0c4b65c588033227bd2786a72`  
		Last Modified: Tue, 19 May 2026 20:22:15 GMT  
		Size: 35.1 KB (35114 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; ppc64le

```console
$ docker pull nginx@sha256:a3e5a84960863a7ba3cc48305d08d8986a6712f5a4a5e739c18a95f552109511
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.2 MB (77154760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:940ba0f64bc52b0a2873445ca1ab9b86c6e78e05138fdd6c7261012e855731fe`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 20:28:37 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:28:37 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:28:37 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 20:28:37 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 19 May 2026 20:28:37 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 20:28:37 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:28:37 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:28:37 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="9d879d57ef75661eaed35e787ef434b2f85771f6"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:28:38 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:28:38 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:28:38 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:28:38 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:28:39 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:28:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:28:39 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:28:39 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:28:39 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:b9baa45d89920bd180d7551ccc5bc535e0c5f55b863ddebddfdc06f9436dfe91`  
		Last Modified: Fri, 08 May 2026 19:46:53 GMT  
		Size: 33.6 MB (33598087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f14da1318918a58aaaf3dd1bbb64d1102b1c2211336a000fc72d8dae45efe3d4`  
		Last Modified: Tue, 19 May 2026 20:29:07 GMT  
		Size: 43.6 MB (43552073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74d37637c0f86fe1abd696200e229024cd390edeb4089f4633ff3ecf0203ccf4`  
		Last Modified: Tue, 19 May 2026 20:29:05 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95e1a7d82c2c655cb2da9547976026508bc39efa16408d2d725f0db84c39a232`  
		Last Modified: Tue, 19 May 2026 20:29:05 GMT  
		Size: 957.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35ceb25f7079816ec80efb2b0953f966a1e2cd500414a070137a35650b53c0b2`  
		Last Modified: Tue, 19 May 2026 20:29:06 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b58c1290b62e860ff0f883473b4eae3f005ff0b34a275b2a61d43285b3c25164`  
		Last Modified: Tue, 19 May 2026 20:29:07 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:639f4dbcdfc0410d61e32a6660d453abe8d6b7169078dfe0d369d698abdb7525`  
		Last Modified: Tue, 19 May 2026 20:29:07 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:eb589ce7ffdf66da70e4c0a162b3eb6fd9b8743392ef760e6221dc88c88c106f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2880120 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2950bb4ad8c7fd3e70b97fc77224a8d4a7c565215d555384f5037bccac2c637`

```dockerfile
```

-	Layers:
	-	`sha256:5b7d1e4fe891c3f41abf9f0ea2da4b77ec0293e5173c1786624fd409a46c2e89`  
		Last Modified: Tue, 19 May 2026 20:29:06 GMT  
		Size: 2.8 MB (2844863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:edf5a15bde1af5bff1d3784caf4e35244be5647463016173b08f1afded723dda`  
		Last Modified: Tue, 19 May 2026 20:29:05 GMT  
		Size: 35.3 KB (35257 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; riscv64

```console
$ docker pull nginx@sha256:a1ba7aeb2ca7d83f235b259f52a80a37c2b88b4c7b33f69ebc07fecf01ab8796
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.7 MB (57729749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb926597e280c0a8a067295d1dab89aa452c5295a5055107756f28122b725b7`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1777939200'
# Thu, 14 May 2026 06:38:40 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Thu, 14 May 2026 06:38:40 GMT
ENV NGINX_VERSION=1.31.0
# Thu, 14 May 2026 06:38:40 GMT
ENV NJS_VERSION=0.9.8
# Thu, 14 May 2026 06:38:40 GMT
ENV NJS_RELEASE=1~trixie
# Thu, 14 May 2026 06:38:40 GMT
ENV ACME_VERSION=0.4.1
# Thu, 14 May 2026 06:38:40 GMT
ENV PKG_RELEASE=1~trixie
# Thu, 14 May 2026 06:38:40 GMT
ENV DYNPKG_RELEASE=1~trixie
# Thu, 14 May 2026 06:38:40 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="7c1dddf7d510642b6f352a16e4c8d7696c791a042cf9758282498d8bc8ae0760263874fbcbbadc420129b15701b32c50cebdc432ad9d2adb9776600b42cfb149 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:38:40 GMT
COPY docker-entrypoint.sh / # buildkit
# Thu, 14 May 2026 06:38:40 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:38:40 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:38:41 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:38:41 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Thu, 14 May 2026 06:38:41 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Thu, 14 May 2026 06:38:41 GMT
EXPOSE map[80/tcp:{}]
# Thu, 14 May 2026 06:38:41 GMT
STOPSIGNAL SIGQUIT
# Thu, 14 May 2026 06:38:41 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:1e9edef871271ebe58c5a713c7c062e88ff414be0976a2c7baf0aba83823c954`  
		Last Modified: Fri, 08 May 2026 20:38:39 GMT  
		Size: 28.3 MB (28280232 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a4f0223b63487848e740e4cfb4093a5a5652d1fb1c6f9b504d86400f336e083`  
		Last Modified: Thu, 14 May 2026 06:40:09 GMT  
		Size: 29.4 MB (29444913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd131e0eac8863ffb7b607f856ed4d3076666e58c62d87c507eb113a1addafdf`  
		Last Modified: Thu, 14 May 2026 06:40:05 GMT  
		Size: 626.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c45152bec58a84e78c83605375a820f2cb90b48fdd961c1b259591c27aef163`  
		Last Modified: Thu, 14 May 2026 06:40:05 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cc8c4b01d626fddd09f642477e6f228f722ec377891315133379442c5d1e8c1`  
		Last Modified: Thu, 14 May 2026 06:40:05 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7aebe9b44cb16155c70a858c8d5d492873ffe19345f95ceb4a95bfd09c13c07a`  
		Last Modified: Thu, 14 May 2026 06:40:06 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a985a8552ee4076f906e7efee00d5b9a4ca6aad53f3062a43b68d5a93ec1037`  
		Last Modified: Thu, 14 May 2026 06:40:06 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:97e1684ff29b7afe6e037cfe0356321df94907425a88fb12c0722d86646c6e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b5e10110ce7be46477f4383e0a6580add37d7cfc5353e9a84a3978ff9041e4f`

```dockerfile
```

-	Layers:
	-	`sha256:9e7f1504c118f9d77d68c6bc516fe40f259018e0ebadd38ab7de2950e0b55efe`  
		Last Modified: Thu, 14 May 2026 06:40:05 GMT  
		Size: 2.8 MB (2834614 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79739a891e11b7d43323809e53a9206a5361008d74cd8504be9bec26f40c93fc`  
		Last Modified: Thu, 14 May 2026 06:40:05 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline-trixie` - linux; s390x

```console
$ docker pull nginx@sha256:1126251da54671cccbbc21b4c887b62344dbe503dd06225adde1d5c9b21f9e10
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68462004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:186d9d54d1220ac16016331283500c75b1a4d2451b30f846437d2e27650ec98e`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Tue, 05 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1777939200'
# Tue, 19 May 2026 20:22:03 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 19 May 2026 20:22:03 GMT
ENV NGINX_VERSION=1.31.0
# Tue, 19 May 2026 20:22:03 GMT
ENV NJS_VERSION=0.9.9
# Tue, 19 May 2026 20:22:03 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:03 GMT
ENV ACME_VERSION=0.4.1
# Tue, 19 May 2026 20:22:03 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:03 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 19 May 2026 20:22:03 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="9d879d57ef75661eaed35e787ef434b2f85771f6"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="8ce2d49f0e61d83d84aa3ae9e16a996bacb3f327c977a12c03a4dd4f9eaf2c9a4c41f4aadb24260fad0b7acdd8907e4d9ef9a1ef0e69c9070849bcdcb5919d61 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:03 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 19 May 2026 20:22:04 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:04 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:04 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:04 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 19 May 2026 20:22:04 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 19 May 2026 20:22:04 GMT
EXPOSE map[80/tcp:{}]
# Tue, 19 May 2026 20:22:04 GMT
STOPSIGNAL SIGQUIT
# Tue, 19 May 2026 20:22:04 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:2fbbc68c452b3ba3a496488f38159dac53afe693311bee1c04f555d854ff4a2e`  
		Last Modified: Fri, 08 May 2026 18:29:20 GMT  
		Size: 29.8 MB (29840347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e12c4476bed069b09e7c33e70f2530854274d72e371e3ffb4b966847986d438c`  
		Last Modified: Tue, 19 May 2026 20:22:20 GMT  
		Size: 38.6 MB (38617058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a22504df55e50b17f6132a7aebe11078693740fd6e3fff75bc636d1f73353894`  
		Last Modified: Tue, 19 May 2026 20:22:20 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d63daefb08c527d8fc167dc26cd8d6e36c8d88cf7c5e4cc63c7920529158edf6`  
		Last Modified: Tue, 19 May 2026 20:22:20 GMT  
		Size: 956.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8ab4b46067b0ab4ef054373d17127efd4ce15a31257ccce2d992f6a1d68e680`  
		Last Modified: Tue, 19 May 2026 20:22:19 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c8ccf8bb2e466a83ad6199898d15e1a69f9406c70ec86a4dbb4cb4bb3c045c2`  
		Last Modified: Tue, 19 May 2026 20:22:20 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c021c868c4d947118de7fcaa17f1213b0eb18e1d2561d2d40a5d839356751790`  
		Last Modified: Tue, 19 May 2026 20:22:21 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline-trixie` - unknown; unknown

```console
$ docker pull nginx@sha256:e57ba17c4c7348f9eda429868c63573bf8458b0279a1f2f42ada420bcfcd638a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 MB (2785796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a641e183277da50596a7819614f9bfa7bd69e5f76d37b100692ee3c97102e30d`

```dockerfile
```

-	Layers:
	-	`sha256:ffae7b2bdb48514b209d81675d57603761d7183ecb4c2820909755b89a3c6144`  
		Last Modified: Tue, 19 May 2026 20:22:19 GMT  
		Size: 2.8 MB (2750619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f9ae245e9772fa46f640332829ce1c3748c8df018d300b29a258beb8c591c00`  
		Last Modified: Tue, 19 May 2026 20:22:19 GMT  
		Size: 35.2 KB (35177 bytes)  
		MIME: application/vnd.in-toto+json
