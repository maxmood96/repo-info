## `nginx:mainline`

```console
$ docker pull nginx@sha256:97da99a1f02cefee7a3cb9c36d828171e2a8c65ebf25c5c4577ef3e0be107f46
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
$ docker pull nginx@sha256:a6bead2c897e9e39ca1a2dbd241f96dc181c8d32adcb6201258624fb37d2c7fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62938940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99133eed2307147a04b4ad4a37582c76a9c5c76ae3d9aad90bec0f4b8878d4c0`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 10 Mar 2026 22:32:09 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 10 Mar 2026 22:32:09 GMT
ENV NGINX_VERSION=1.29.6
# Tue, 10 Mar 2026 22:32:09 GMT
ENV NJS_VERSION=0.9.6
# Tue, 10 Mar 2026 22:32:09 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:32:09 GMT
ENV ACME_VERSION=0.3.1
# Tue, 10 Mar 2026 22:32:09 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:32:09 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 10 Mar 2026 22:32:09 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="4cfaf8725bdead3e1944f91af7d97e8102892a205cccd1b0e4de6588f3f8a8171c0d856f27cc8bdd5ffd063adec3a57b85cf82fbb13cba0dd8bf902f40be5715 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 10 Mar 2026 22:32:09 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 10 Mar 2026 22:32:09 GMT
EXPOSE map[80/tcp:{}]
# Tue, 10 Mar 2026 22:32:09 GMT
STOPSIGNAL SIGQUIT
# Tue, 10 Mar 2026 22:32:09 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75a1d70aee5027b89aeb5eec54823d28982ec97ade2fc5d8837281ecee4dc7af`  
		Last Modified: Tue, 10 Mar 2026 22:32:19 GMT  
		Size: 33.2 MB (33155717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9d395129dcefbfb212cd08db7cf1f70d256eefd83c2458c45e18a365b0a5bd0`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df9da45c1db2401fec7485da87d95235e97e1824cb70c5900fea4fb74a87ba6f`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 954.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18a071c04bd15da01eff3b9f14e784c765ae4e2220ba2041a02d51d55e53e091`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 403.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79697674b8970919d82181f2856f2494024570b22db3103cc062d6552eccddbd`  
		Last Modified: Tue, 10 Mar 2026 22:32:19 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9eef040df109a68da4ee0f20ef79c6a5a3b4942ac19e68422e785632684fcde3`  
		Last Modified: Tue, 10 Mar 2026 22:32:19 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:33564df5f8f5334b28e25be085c93e4251e83398232733f3776506cd40cff297
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2852379 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e61214808975770e4a3b07c2d5a37519c1e86a7959510f4e1e28e1a4ccb67885`

```dockerfile
```

-	Layers:
	-	`sha256:23abb0f9ce55dfc5488fc6045c4edb58ca7369e5dd7f721df501c1d7e7518728`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 2.8 MB (2817223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d99947bc9177029fd2595346665ac75b32350d2ef34808c806d61c28bec94005`  
		Last Modified: Tue, 10 Mar 2026 22:32:18 GMT  
		Size: 35.2 KB (35156 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; arm variant v5

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

### `nginx:mainline` - unknown; unknown

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

### `nginx:mainline` - linux; arm variant v7

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

### `nginx:mainline` - unknown; unknown

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

### `nginx:mainline` - linux; arm64 variant v8

```console
$ docker pull nginx@sha256:f676e65a102e4eb6b30ca6ece7300e1ad72bdd60758b8e4e5072c45b86979916
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.2 MB (61248242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0000f06a0cafed8b95a6dabaec83c50aa674280ffb0e9ee3ff87521518580bcc`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:08:26 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Feb 2026 19:08:26 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 24 Feb 2026 19:08:26 GMT
ENV NJS_VERSION=0.9.5
# Tue, 24 Feb 2026 19:08:26 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:08:26 GMT
ENV ACME_VERSION=0.3.1
# Tue, 24 Feb 2026 19:08:26 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:08:26 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:08:26 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:26 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 19:08:26 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:27 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:27 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:27 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:08:27 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:08:27 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:08:27 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:08:27 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a89256e588a59c19954ebc8a66aa7d464370096f4d7e5b52efde9cfd5d70a2d`  
		Last Modified: Tue, 24 Feb 2026 19:08:36 GMT  
		Size: 31.1 MB (31103547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c813174c999b01107d86097d711f5a38d5dfc40c51192f44b93859528fbf6f66`  
		Last Modified: Tue, 24 Feb 2026 19:08:35 GMT  
		Size: 628.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:901e94f777d19c29bda7ca9a1d6a4761a5a2e0f7ce1ace6caeb60e3268335e5f`  
		Last Modified: Tue, 24 Feb 2026 19:08:35 GMT  
		Size: 955.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88d7844c33ddce38435479107a2bc900d129647ddc6a182bdd7b57f4796f6f8`  
		Last Modified: Tue, 24 Feb 2026 19:08:35 GMT  
		Size: 405.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2668e34349761086c8c3ceb1f269a65e54326d52c5e222c7f686c48825a10cd3`  
		Last Modified: Tue, 24 Feb 2026 19:08:36 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c05cdfb14987a928321a4e4fd9386113f00e4f7acaf43aa08716680a704f46`  
		Last Modified: Tue, 24 Feb 2026 19:08:36 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:69a8ea3c9df1c5a11d9649e9092a438128ccd1870013549638310cf24bbc590c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2853039 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d041242a1b630195ca84d34d22c016129bdf314b91e10145cb440fcf4c0c811d`

```dockerfile
```

-	Layers:
	-	`sha256:35dee7ece0462e8ac3045b75893a8be4f4a8698684e9caabb207b1a47142e8ca`  
		Last Modified: Tue, 24 Feb 2026 19:08:36 GMT  
		Size: 2.8 MB (2817707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c9c97ab7d80761e95421a886b533e97bbf4a35577f0d6bf9084f725fb714d7b`  
		Last Modified: Tue, 24 Feb 2026 19:08:35 GMT  
		Size: 35.3 KB (35332 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; 386

```console
$ docker pull nginx@sha256:289fbb3748210f4880d7c4c5701c45eee3626bebbf662f450c6ef74ddacf5c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63297954 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7e73bd4935b27aab08e0696c92226a8ead683db9d4813a8e95090ef3efb039a`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:06:22 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Tue, 24 Feb 2026 19:06:22 GMT
ENV NGINX_VERSION=1.29.5
# Tue, 24 Feb 2026 19:06:22 GMT
ENV NJS_VERSION=0.9.5
# Tue, 24 Feb 2026 19:06:22 GMT
ENV NJS_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:06:22 GMT
ENV ACME_VERSION=0.3.1
# Tue, 24 Feb 2026 19:06:22 GMT
ENV PKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:06:22 GMT
ENV DYNPKG_RELEASE=1~trixie
# Tue, 24 Feb 2026 19:06:22 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:06:22 GMT
COPY docker-entrypoint.sh / # buildkit
# Tue, 24 Feb 2026 19:06:22 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:06:23 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:06:23 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:06:23 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Tue, 24 Feb 2026 19:06:23 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Tue, 24 Feb 2026 19:06:23 GMT
EXPOSE map[80/tcp:{}]
# Tue, 24 Feb 2026 19:06:23 GMT
STOPSIGNAL SIGQUIT
# Tue, 24 Feb 2026 19:06:23 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d899e3c47247ed00600546f97744b86498e4a086459fcc1404bad45a209fd2a7`  
		Last Modified: Tue, 24 Feb 2026 19:06:33 GMT  
		Size: 32.0 MB (31999431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb070e6e7be2a2866cdda793ef18509c0e06501d020f194f1bc3ff9809057306`  
		Last Modified: Tue, 24 Feb 2026 19:06:32 GMT  
		Size: 629.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de0ef58cccc32ca3db67256f917f830e02ab0412ef05e6c284e11cf19ecf8683`  
		Last Modified: Tue, 24 Feb 2026 19:06:32 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bbe0c85063c74518a5a32c456a85ae126aa778dfd3b1ea6048851eff9d4bd75`  
		Last Modified: Tue, 24 Feb 2026 19:06:32 GMT  
		Size: 406.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df88e10ff841030aca7972873e3de80cbee1d3ef10ff678e08722a69a2e45530`  
		Last Modified: Tue, 24 Feb 2026 19:06:33 GMT  
		Size: 1.2 KB (1212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cfa51a35acf0bd88fd2fd0aca4f0b674972ff0922cef47e67a506c868d0f135`  
		Last Modified: Tue, 24 Feb 2026 19:06:33 GMT  
		Size: 1.4 KB (1400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:a853de95da7c7c3b43ac30d55d726a0b7bb0d7027070616a1339d3c1ca931073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2872152 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0903fe6a780ce8d824b4ef96f872267bc4f2e5203f5d178a28134d77768380`

```dockerfile
```

-	Layers:
	-	`sha256:fe8efedf3217a5996ce2c3ffc0a78ec2425e4bcaf4d1a40e19792085a860c405`  
		Last Modified: Tue, 24 Feb 2026 19:06:32 GMT  
		Size: 2.8 MB (2837059 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5134065ed1502cfc0f0b7fd78faacf9937b0dc34473f19822546e0c2668b54c`  
		Last Modified: Tue, 24 Feb 2026 19:06:32 GMT  
		Size: 35.1 KB (35093 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; ppc64le

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

### `nginx:mainline` - unknown; unknown

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

### `nginx:mainline` - linux; riscv64

```console
$ docker pull nginx@sha256:d3d3ee5379774d1872e4fdb9f2a06184f05e456bd39afbe7381f32334481b09e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.6 MB (57611417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb68f1ebb4fbc9282a064d11889f8b8c54bb6ef33eabb4456d2bc87768a2cd43`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["nginx","-g","daemon off;"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1771804800'
# Wed, 25 Feb 2026 06:00:39 GMT
LABEL maintainer=NGINX Docker Maintainers <docker-maint@nginx.com>
# Wed, 25 Feb 2026 06:00:39 GMT
ENV NGINX_VERSION=1.29.5
# Wed, 25 Feb 2026 06:00:39 GMT
ENV NJS_VERSION=0.9.5
# Wed, 25 Feb 2026 06:00:39 GMT
ENV NJS_RELEASE=1~trixie
# Wed, 25 Feb 2026 06:00:39 GMT
ENV ACME_VERSION=0.3.1
# Wed, 25 Feb 2026 06:00:39 GMT
ENV PKG_RELEASE=1~trixie
# Wed, 25 Feb 2026 06:00:39 GMT
ENV DYNPKG_RELEASE=1~trixie
# Wed, 25 Feb 2026 06:00:39 GMT
RUN set -x     && groupadd --system --gid 101 nginx     && useradd --system --gid nginx --no-create-home --home /nonexistent --comment "nginx user" --shell /bin/false --uid 101 nginx     && apt-get update     && apt-get install --no-install-recommends --no-install-suggests -y gnupg1 ca-certificates     &&     NGINX_GPGKEYS="573BFD6B3D8FBC641079A6ABABF5BD827BD9BF62 8540A6F18833A80E9C1653A42FD21310B49F6B46 9E9BE90EACBCDE69FE9B204CBCDCD8A38D88A2B3";     NGINX_GPGKEY_PATH=/etc/apt/keyrings/nginx-archive-keyring.gpg;     export GNUPGHOME="$(mktemp -d)";     found='';     for NGINX_GPGKEY in $NGINX_GPGKEYS; do     for server in         hkp://keyserver.ubuntu.com:80         pgp.mit.edu     ; do         echo "Fetching GPG key $NGINX_GPGKEY from $server";         gpg1 --batch --keyserver "$server" --keyserver-options timeout=10 --recv-keys "$NGINX_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $NGINX_GPGKEY" && exit 1;     done;     gpg1 --batch --export $NGINX_GPGKEYS > "$NGINX_GPGKEY_PATH" ;     rm -rf "$GNUPGHOME";     apt-get remove --purge --auto-remove -y gnupg1 && rm -rf /var/lib/apt/lists/*     && dpkgArch="$(dpkg --print-architecture)"     && nginxPackages="         nginx=${NGINX_VERSION}-${PKG_RELEASE}         nginx-module-xslt=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-geoip=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-image-filter=${NGINX_VERSION}-${DYNPKG_RELEASE}         nginx-module-njs=${NGINX_VERSION}+${NJS_VERSION}-${NJS_RELEASE}         nginx-module-acme=${NGINX_VERSION}+${ACME_VERSION}-${PKG_RELEASE}     "     && case "$dpkgArch" in         amd64|arm64)             echo "deb [signed-by=$NGINX_GPGKEY_PATH] https://nginx.org/packages/mainline/debian/ trixie nginx" >> /etc/apt/sources.list.d/nginx.list             && apt-get update             ;;         *)             tempDir="$(mktemp -d)"             && chmod 777 "$tempDir"                         && savedAptMark="$(apt-mark showmanual)"                         && apt-get update             && apt-get install --no-install-recommends --no-install-suggests -y                 cargo                 curl                 devscripts                 equivs                 git                 libxml2-utils                 lsb-release                 xsltproc             && (                 cd "$tempDir"                 && export CARGO_HOME="$tempDir/.cargo"                 && REVISION="${NGINX_VERSION}-${PKG_RELEASE}"                 && REVISION=${REVISION%~*}                 && curl -f -L -O https://github.com/nginx/pkg-oss/archive/${REVISION}.tar.gz                 && PKGOSSCHECKSUM="b8584eaa97130ba7743dfbb2a10f665d64cb54b864e2038d0fd298d24682fc05eb4472738430b15862dabc6f374917f1b9889117051a852d36d0a6c8bc898921 *${REVISION}.tar.gz"                 && if [ "$(openssl sha512 -r ${REVISION}.tar.gz)" = "$PKGOSSCHECKSUM" ]; then                     echo "pkg-oss tarball checksum verification succeeded!";                 else                     echo "pkg-oss tarball checksum verification failed!";                     exit 1;                 fi                 && tar xzvf ${REVISION}.tar.gz                 && cd pkg-oss-${REVISION}                 && cd debian                 && for target in base module-geoip module-image-filter module-njs module-xslt module-acme; do                     make rules-$target;                     mk-build-deps --install --tool="apt-get -o Debug::pkgProblemResolver=yes --no-install-recommends --yes"                         debuild-$target/nginx-$NGINX_VERSION/debian/control;                 done                 && make base module-geoip module-image-filter module-njs module-xslt module-acme             )                         && apt-mark showmanual | xargs apt-mark auto > /dev/null             && { [ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; }                         && ls -lAFh "$tempDir"             && ( cd "$tempDir" && dpkg-scanpackages . > Packages )             && grep '^Package: ' "$tempDir/Packages"             && echo "deb [ trusted=yes ] file://$tempDir ./" > /etc/apt/sources.list.d/temp.list             && apt-get -o Acquire::GzipIndexes=false update             ;;     esac         && apt-get install --no-install-recommends --no-install-suggests -y                         $nginxPackages                         gettext-base                         curl     && apt-get remove --purge --auto-remove -y && rm -rf /var/lib/apt/lists/* /etc/apt/sources.list.d/nginx.list         && if [ -n "$tempDir" ]; then         apt-get purge -y --auto-remove         && rm -rf "$tempDir" /etc/apt/sources.list.d/temp.list;     fi     && ln -sf /dev/stdout /var/log/nginx/access.log     && ln -sf /dev/stderr /var/log/nginx/error.log     && mkdir /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:39 GMT
COPY docker-entrypoint.sh / # buildkit
# Wed, 25 Feb 2026 06:00:39 GMT
COPY 10-listen-on-ipv6-by-default.sh /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:39 GMT
COPY 15-local-resolvers.envsh /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:39 GMT
COPY 20-envsubst-on-templates.sh /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:40 GMT
COPY 30-tune-worker-processes.sh /docker-entrypoint.d # buildkit
# Wed, 25 Feb 2026 06:00:40 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 25 Feb 2026 06:00:40 GMT
EXPOSE map[80/tcp:{}]
# Wed, 25 Feb 2026 06:00:40 GMT
STOPSIGNAL SIGQUIT
# Wed, 25 Feb 2026 06:00:40 GMT
CMD ["nginx" "-g" "daemon off;"]
```

-	Layers:
	-	`sha256:7d614b9ad5a6f3dd0478c6903a6d2ffddc9bc5b17650714d4c1f761161fde58d`  
		Last Modified: Tue, 24 Feb 2026 18:59:14 GMT  
		Size: 28.3 MB (28276417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a69861c59b95c20d8a221aff7b4dbfec2c74dde6aed0c0e0245366a6e7c33a1d`  
		Last Modified: Wed, 25 Feb 2026 06:02:10 GMT  
		Size: 29.3 MB (29330398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78b00fab1172b9d73b6b47a2cf46ff4fbb809feebdcbce383ea6452ea876aafb`  
		Last Modified: Wed, 25 Feb 2026 06:02:05 GMT  
		Size: 627.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07033ca0e3f64c5812dd1abd8b4358cbef6c3237541d4f4d69a000bacee62b18`  
		Last Modified: Wed, 25 Feb 2026 06:02:05 GMT  
		Size: 958.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f89c5fb920fd68b332a9c61a89be3b2f198692d169f182ca052dab2ec43ae9`  
		Last Modified: Wed, 25 Feb 2026 06:02:05 GMT  
		Size: 407.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45e5e32157228f18e91b085287ff4c49b185432172e2beb78bf5e8482a0abb3c`  
		Last Modified: Wed, 25 Feb 2026 06:02:07 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4f12e7fecac12875c0591a19f2c763bcac04ea78fdd3c087955506cad79288e`  
		Last Modified: Wed, 25 Feb 2026 06:02:07 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `nginx:mainline` - unknown; unknown

```console
$ docker pull nginx@sha256:3a76b67783924ccf7b5f7089cf31886976547e02488db4ab9ac5ca2aab6e875a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.9 MB (2869776 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f09049cabafe28055d1801d907d44cca46fa690b2e562cd6d754f141edb46ae`

```dockerfile
```

-	Layers:
	-	`sha256:9531c8a57dc009b702d8e096f23024cbc89e54d65bbf13ea486537073bc7ddbb`  
		Last Modified: Wed, 25 Feb 2026 06:02:06 GMT  
		Size: 2.8 MB (2834540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7d4f949d8048eb05f85cb8e14ecfca821c2d916616c0a03f5f64a23709fb6af`  
		Last Modified: Wed, 25 Feb 2026 06:02:05 GMT  
		Size: 35.2 KB (35236 bytes)  
		MIME: application/vnd.in-toto+json

### `nginx:mainline` - linux; s390x

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

### `nginx:mainline` - unknown; unknown

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
